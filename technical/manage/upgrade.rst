.. _upgrade_server:

Upgrading OppiaMobile Server
=============================

To ensure you get all the latest features, bug fixes and patches, it's important to keep your OppiaMobile server up to
date.

The upgrade process is described below, with the paths/directories described as OppiaMobile server is set up on the AWS
image. If you have installed  OppiaMobile server to different location, then amend the paths/directories as required.
Or, if you have your own clone of the OppiaMobile server code, you will need to merge the core version into your clone
and resolve any conflicts, before updating your server.

Your server must be connected to the internet for the upgrade process.

Backup
-------

Ensure you have a backup of your OppiaMobile database, code and any uploaded files/courses

Pull the latest updates from the core version
----------------------------------------------

#. Move to the django-oppia directory: ``$ cd /home/oppiamobile/django-oppia/``
#. Pull the latest updates: ``$ sudo git pull``

Activate the VirtualEnv
--------------------------

#. Move to Oppia directory: ``$ cd /home/oppiamobile``
#. Activate virtual environment: ``$ source env/bin/activate``

You will see the prefix ``(env)`` at the beginning of your command line. Once the upgrade is complete you can 
de-activate the virtual environment using ``(env)$ deactivate``.

Check for any updated/new required packages
---------------------------------------------

#. Check and install: ``(env)$ pip install -r django-oppia/requirements.txt``

Any updated or new packages will now be installed

Migrate the database
-----------------------

#. Migrate database with: ``(env)$ python django-oppia/manage.py migrate``

Copy static files
------------------

#. Copy static files with: ``(env)$ python manage.py collectstatic``

Run update_summaries --fromstart
---------------------------------

This isn't necessary for every release unless specified. But if you are skipping quite a few inbetween releases (e.g.
from 0.12.2 to 0.13.3), then it's best to run this.

#. Run the update summaries command from start: ``(env)$ python manage.py update_summaries --fromstart``
#. This might take a long time (hours) for large implementations, see :doc:`/technical/manage/update-summaries`


Restart Apache
------------------

#. Restart Apache server: ``$ sudo service apache2 restart``


Additional Updates
-------------------

Some releases may have some additional specific upgrade steps. Releases (from 0.12.0 onwards) that have additional
steps are noted below. 

* v0.12.22
* v0.12.24
