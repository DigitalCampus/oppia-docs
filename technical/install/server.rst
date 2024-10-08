.. _manualinstall:

Server - Manual Installation
==============================

To manual install and run an OppiaMobile server, e.g. as a local development
server or as live server running on a locally hosted server. Please follow the
instructions below.

Prerequisites
-----------------

It would be helpful if you had some system admin/set up experience before, and 
please note that these instructions are based on using Ubuntu as the 
operating system, with MySQL for the database server and Apache2 as the 
webserver. If you are using a different operating system, database or 
webserver, then some of the exact commands may differ a little.

You should have some familiarity with `Git <https://git-scm.com/>`_ and have 
this installed on your machine.

1. Set up empty database
------------------------

We generally use MySQL for the database, but Oppia will support any database
platform that Django supports (see: 
https://docs.djangoproject.com/en/2.1/ref/databases/ for more detailed notes)

In the MySQL command line, run::

	> create database oppia default character set utf8mb4;
	> grant all privileges on oppia.* to 'oppiauser'@'localhost' identified by 
		'yourpassword';
	> flush privileges;
	> quit

The database name, username and password can be whatever you like.

2. Clone the code and add custom settings
------------------------------------------

Select or create a suitable directory on your file system, for the rest of this 
setup. We use ``/home/oppia/``, but you may prefer something like 
``/var/html/oppia/``. The rest of these instructions will assume you are using 
``/home/oppia/``, so edit any of the following commands/settings as necessary
if you're using something different.

#. Navigate to your selected directory
#. Run::
	
    $ git clone https://github.com/DigitalCampus/django-oppia.git
	
   If you have your own fork of the Oppia code, then replace the location with 
   your own fork's url.
   
#. This will create a directory ``/home/oppia/django-oppia/`` with the latest
   stable release version of the Oppia server code.   
#. Navigate to the ``/home/oppia/django-oppia/oppiamobile/`` directory
#. Copy the ``settings_secret.py.template`` to ``settings_secret.py``, eg:
   by using::
   
   	$ cp settings_secret.py.template settings_secret.py

#. Open the ``settings_secret.py`` file in your favourite text editor and
   update at least the following settings:
   
   #. Database name, user, password (that you created in step 1 above)
   #. ``SECRET_KEY``: This can be anything you like, generally a long list of
      random characters.
   #. ``ADMINS`` and ``SERVER_EMAIL``: update these to your system admin details
   #. ``ALLOWED_HOSTS``: to be able to access externally the Django app, you need to
      add your hostname to the list of allowed hosts. You can also use the ``*``
      wildcard in a debug server.


   In this file you can also override any of the settings in
   ``/home/oppia/django-oppia/oppiamobile/settings.py``
   
#. Save your ``settings_secret.py`` file
    
    
3. Install Ubuntu packages
---------------------------

Some additional packages are required that are not included on a default 
installation of Ubuntu, so you'll need to install these:

#. ``sudo apt-get install python3-mysqldb python3-dev libpython3-dev`` - 
   extra python3 packages
#. ``sudo apt-get install libjpeg-dev zlib1g-dev`` - extra packages for images
#. ``sudo apt-get install ffmpeg`` - for analysing uploaded media files
   
4. Set up virtualenv and packages
-----------------------------------

`VirtualEnv <https://pypi.python.org/pypi/virtualenv/>`_  is a way to sandbox
your python libraries so they are not affected by other updates or versions
that you may be using for other services and applications on your machine. You
don't have to use this, but it is very strongly recommended that you download
and install this to use.

#. Navigate to ``/home/oppia/`` and run::
	
	$ virtualenv -p /usr/bin/python3 env
	
#. Run::

	$ source env/bin/activate
	
   Your command line should now look something like::
  
    (env)$


#. Install the required packages for the Oppia server by running::

    (env)$ pip install -r django-oppia/requirements.txt
    
   This may take some time as it downloads and sets up all the necessary
   python libraries that are required by the Oppia server.

#. Install a database connector, since we use MySQL, the command below is 
   specifically for that database server. If you are using a different database 
   server, then use the appropriate one for your database server::
   
    (env)$ pip install mysqlclient

#. Some python packages are compiled against system libraries (for example,
   the Pillow imaging library). If the previous command fails at some of
   the installations, try installing these packages and then try again.::

    (env)$ sudo apt-get install build-essential checkinstall 
    libreadline-gplv2-dev openssl libncursesw5-dev libgdbm-dev 
    libc6-dev libbz2-dev python-dev libmysqlclient-dev

   In some cases, it will be required to perform a system reboot for this
   changes to be applied.


#. You should now have all the required libraries set up and installed. 


5. Set up other directories and permissions
---------------------------------------------

Create directories for media, static and uploads by running (from 
``/home/oppia/``)::
	
	$ mkdir media
	$ mkdir static
	$ mkdir upload

If you are going to run this Oppia server as a live server, you should make 
sure that your webserver user (eg www-data) had read and write access to all
these directories.

6. Initialise the database and add admin user
-----------------------------------------------

Now to create the database structure and an initial admin user.

#. Navigate the ``/home/oppia/django-oppia/`` directory
#. Create the database by running::

	(env)$ python manage.py migrate
	
#. Load initial data::

	(env)$ python manage.py loaddata oppia/fixtures/default_badges.json
	(env)$ python manage.py loaddata oppia/fixtures/default_gamification_events.json

#. Compile the SCSS file::

	(env)$ python manage.py compilescss
	
#. Copy the static files with::

	(env)$ python manage.py collectstatic

#. Create a first admin user with::

	(env)$ python manage.py createsuperuser

   and follow the instructions. After you have create an admin on the command
   line, you will also need to create a user profile for them. To do this go to
   the Django admin at <your-site>/admin, log in and add a user profile record.

7. Run the tests (optional but recommended)
---------------------------------------------

To check that everything has been set up and installed correctly, you can run 
the automated tests using::

	(env)$ python manage.py test

8. Test running the server locally
-------------------------------------

Check that the server will run properly on the local machine, by running::

	(env)$ python manage.py runserver

Then, in the web browser on the same machine, open::

	http://localhost:8000 


9. Configure web server (for live servers)
--------------------------------------------

If the Oppia server you are setting up is to run as a live server, then you 
will need to configure your web server.

As mentioned above, these instructions assume that you are using Apache 
webserver, and we use the 
`mod_wsgi <https://modwsgi.readthedocs.io/en/latest/>`_ 
package for serving python applications via Apache, so before proceeding, 
ensure that you have mod_wsgi installed and enabled for your Apache server.

To install and enable WSGI for Python 3 and Apache, run::

	$ sudo apt-get install libapache2-mod-wsgi-py3

Here is an example Apache config file that you can use and adapt::

	<VirtualHost *:80>
	
		ServerName localhost.oppia
		WSGIDaemonProcess localhost.oppia python-path=/home/oppia/django-oppia:/home/oppia/env/lib/python3.6/site-packages
		WSGIProcessGroup localhost.oppia
		WSGIScriptAlias / /home/oppia/django-oppia/oppiamobile/wsgi.py
		WSGIPassAuthorization On
	
		<Directory /home/oppia/django-oppia/oppiamobile/>
			<Files wsgi.py>
				Require all granted
			</Files>
		</Directory>
	
		Alias /media /home/oppia/media/
	    	<Directory "/home/oppia/media/">
			Options MultiViews FollowSymLinks
			AllowOverride None
			Require all granted
	    	</Directory>
	
		Alias /static /home/oppia/static/
	    	<Directory "/home/oppia/static/">
			Options MultiViews FollowSymLinks
			AllowOverride None
			Require all granted
	    	</Directory>
	
		
	
		LogLevel warn
		ErrorLog /var/log/apache2/oppia-error.log
		CustomLog /var/log/apache2/oppia-access.log combined
	
	</VirtualHost>

Replace the ``ServerName`` ``localhost.oppia`` with your site's domain name and
adjust any instances of ``/home/oppia/`` with the directory you used for 
installing.


10. Configure SSL (recommended)
-----------------------------------------------

It is recommended to set up SSL (HTTPS) certificates for the connection 
between users devices and the server.

You can use `LetsEncrypt <https://letsencrypt.org/>`_ to set up free SSL 
certificates.

.. _manualinstall-email:

11. Configure email (recommended)
------------------------------------


In your ``settings_secret.py`` file, edit the ``EMAIL_BACKEND`` and 
``SERVER_EMAIL`` to configure sending emails from Oppia. 

Exactly how these need to be configured and set up will depend on your email
backend (see: 
https://docs.djangoproject.com/en/2.2/topics/email/#email-backends). For live
servers you are most likely to want to use the `SMTP backend
<https://docs.djangoproject.com/en/2.2/topics/email/#smtp-backend>`_.

.. _installcron:

12. Set up cron task
---------------------

There are 2 scheduled tasks, one does the processing for awarding badges and 
general maintenance (eg clearing old user sessions and temporary files), and the
other to generate the cached data for displaying the dashboard data.

These can be run as a single cron task. We recommend putting this file in your
``/home/oppia/`` directory. ``oppia-cron.sh``::
 
	#!/bin/bash

	cd /home/oppia/
	source env/bin/activate
	
	python django-oppia/manage.py oppiacron --hours=48
	python django-oppia/manage.py update_summaries

	
Edit the sudo users ``crontab`` to run this script regularly - at least once per hour.

13. Contribute!
----------------

If you find issues and have fixed them or have added extra features/
functionality, then please send us a pull request to integrate into the core 
server code so everyone can benefit. If you find an issue, but aren't sure how 
to fix it, then please 
`file an issue on Github <https://github.com/DigitalCampus/django-oppia/issues>`_


