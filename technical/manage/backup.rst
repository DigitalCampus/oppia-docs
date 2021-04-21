Backing up an OppiaMobile server
======================================

There are many different approaches to doing backups, but the key issue is that
your OppiaMobile server is being backed up somehow, and that these backups are
stored or synched to a completely separate machine.

At Digital Campus, we focus on backing up the core database and uploaded files,
as these are the most important. But there are also methods to make incremental 
backups of your whole system (eg through automated AWS snapshots).

Creating backups directly on the server
-----------------------------------------

For taking backups of the core database and uploaded files, this is the approach
we use:

* Create a directory `/home/backup/` directly on the server (or other directory
  that you'd prefer, and amend the paths shown below appropriately) 
* Place into this directory a shell script ``backup.sh``::

	#!/bin/sh
	
	DATE=`date '+%Y-%m-%d-%H-%M'`
	BACKUPDIR="/home/backup/db"
	
	/usr/bin/mysqldump -ubackup -p<password> oppia_db | gzip > $BACKUPDIR"/"$DATE-oppia-db.gz
	
	cd $BACKUPDIR
	/usr/bin/find \( -name "*-oppia-*.gz" \) -mtime +30 -delete
	
	cd /home/backup/
	echo "backup success: "$DATE >> backup.log
	
* Note that you'll need to create a specific user that has access to your
  database, and supply the relevant credentials above
* This script will create daily backups of your Oppia database, and retain them
  for 30 days, you can adjust this as appropriate.
* For backing up the uploaded course files and media, we use ``rsnapshot``
  (https://rsnapshot.org/), with the following configuration (which will usually
  be at ``/etc/rsnapshot.conf``), we've left out the whole configuration script,
  below only contains the specific updates we've made::

    ###########################
	# SNAPSHOT ROOT DIRECTORY #
	###########################
	
	# All snapshots will be stored under this root directory.
	#
	snapshot_root	/home/backup/rsnapshot/
	
	...

  	#########################################
	#     BACKUP LEVELS / INTERVALS         #
	# Must be unique and in ascending order #
	# e.g. alpha, beta, gamma, etc.         #
	#########################################

  	retain	alpha	31
	#retain	beta	7
	#retain	gamma	4
	#retain	delta	3
	
	...
	
	###############################
	### BACKUP POINTS / SCRIPTS ###
	###############################
	
	# LOCALHOST
	backup	/home/www/oppia-uploads/	localhost/
	backup	/home/www/media/		localhost/
	
* You may need to amend the backup points paths, depending on where you have
  installed the Oppia server. As with the database backup, this retains the
  backups for one month
* We then update our cron script to run these database and file backups
  overnight::

	######
	# BACKUP
	######
	3 4 * * * /home/backup/backup.sh
	42 4 * * * /usr/bin/rsnapshot alpha

Synching backups to an offsite machine
------------------------------------------

The above process and scripts will create the backups, but these are still
directly on the same machine that Oppia is running on. This is far from ideal
if there is a complete system failure, as you will then not even be able to
access your backups. So for this, the backups should then be synched to another
machine.

To do this, we use ``rsych`` (https://rsync.samba.org/) running on the remote
server/machine to copy the local Oppia backups onto this machine, eg::

	#!/bin/sh
	
	start=`date +%s`
	
	echo '#################'
	echo '# Oppia'
	echo '#################'
	/usr/bin/rsync -avzH -e ssh --numeric-ids --delete ubuntu@<IP/domain name of your server>:/home/backup/ /home/remote/backup/aws/oppia/ 
	
	end=`date +%s`
	runtime=$((end-start))
	echo `date`" AWS success - Oppia  - $runtime seconds" >> /home/remote/data/backup/backup.log

You'll need to provide the IP or domain name of your server for the script to
connect, and also ensure this script has access to the remote machine (either
via digital certificate or password). Also amend any paths as appropriate.

You can now set up this rysnc as a cron task on your remote machine.	

After you have got this initially set up, you should check that the backups are
being created correctly and being synced to your remote machine.



