.. _aws:

Installing on Amazon Web Services
=================================

To make it easier for you to get an OppiaMobile server up and running, we have 
created an `Amazon Web Services <http://aws.amazon.com/>`_ machine image that 
you can copy and comes pre-packaged with the latest version of the OppiaMobile 
Server so will run 'out of the box'.


Launch an AWS Machine Image
------------------------------
Once you have created your account on AWS:

* Go into your instances page
* Select 'launch instance'
* Select 'Community AMIs'
* Search for 'oppiamobile' and you should see the most recent version of the 
  OppiaMobile AMI listed
* Launch your new instance - you can alter the instance configuration (security 
  groups etc) during the rest of the launch instance process.
  
.. note::
	When you search the OppiaMobile server AMI will only appear in the search 
	results if you have selected the 'EU (Ireland)' zone

Once your instance is up and running you will be able to assign a static IP, 
access via your web browser and log into the server using the IP address. 

It is beyond the scope of this guide to give the full information about how to
connect and configure your AWS account instances, but in your AWS security
group, you'll need to open up access for both HTTP and HTTPS.

You can point your domain name to the IP address, and edit the Apache config
file: ``/etc/apache2/sites-available/oppia.conf`` to specify your domain name
on the line ``ServerName localhost.oppia``.

Access via SSH
-----------------

It is strongly recommended that you only allow access to your Oppia server using
SSH (HTTPS). Certbot is already installed on the server, so you can
use this to set up free SSH certificates. For more info see: 
`<https://certbot.eff.org/lets-encrypt/ubuntubionic-apache>`_ (start from step 7)

 
Passwords
----------
When you install and launch your instance it is set up with a default set of 
usernames/passwords:

* MySQL root password: 'default'
* MySQL oppia user password: 'default' - this is the user that Django uses to 
  connect to your database. When you have changed this password you should also 
  update the settings file (at: 
  ``/home/oppiamobile/django-oppia/oppiamobile/settings_secret.py``) to reflect the new 
  database password.
* Django super user: username 'admin' and password 'default'
	
.. warning:: 
	You are very strongly advised to change these passwords as soon as 
	you have set up your instance

Directories and location of files
---------------------------------
All the required files are stored in the /home/oppia/ directory, which has 
the following structure:

* django-oppia (dir): the OppiaMobile server application files
* env (dir): root of the `virtualenv <http://www.virtualenv.org/en/latest/>`_
* media (dir): the media directory for Django (this directory served directly by 
  Apache)
* oppia-cron.sh (file): a shell script for running the OppiaMobile cron task - it's 
  unlikely you'll ever need to do anything with this file.
* static (dir): the static directory for Django (this directory is served directly by 
  Apache)
* upload (dir): stores the course uploads

.. warning:: 
	In the main django settings, the server is set to run in debug mode. This will be fine when you are testing, but 
	once you are ready to start providing the server live, you should change this setting to `DEBUG=False`

Updating django-oppia server code from core
--------------------------------------------
The code is based on a 'point-in-time' version of the OppiaMobile server code, 
so once you have set up your instance, you should try to keep it up to date. 

:ref:`View the docs on how to upgrade <upgrade_server>`

Creating your own version of django-oppia
-----------------------------------------
If you have created your own fork of django-oppia (for example to customise the 
look and feel), then you can point git to the fork of your code by editing the 
``/home/oppiamobile/django-oppia/.git/config`` file and pulling the code from 
your fork instead.

:ref:`More information on customising OppiaMobile <custom_server>`

Environment information
-----------------------
The current version of the instance is running:

* OppiaServer 0.15.3
* Ubuntu 22.04 LTS Server
* Apache 2.4
* Mysql 8.0


Email configuration
-------------------
By default your AWS Oppia server is not configured to send email, any 
emails generated by the system (for example reset password messages) are just 
saved as plain text files in the ``/tmp`` directory.

To enable sending email you will need to:

* configure your AWS account to enable email sending (using SES service)
* create/download your AWS IAM Access Key
* update the ``/home/oppiamobile/django-oppia/oppiamobile/settings_secret.py``
  file to configure sending email
  
Your ``settings_secret.py`` file should have a block of code like this (just 
add in your email, access key and secret access key)::

	# Email setup
	SERVER_EMAIL = '<admin@my-oppia-server.org>'
	EMAIL_SUBJECT_PREFIX = '[OppiaMobile]: '
	EMAIL_BACKEND = 'django.core.mail.backends.smtp.EmailBackend'
	
	EMAIL_HOST = 'email-smtp.eu-west-1.amazonaws.com'
	EMAIL_PORT = 587
	EMAIL_HOST_USER = '<IAM Access User>'
	EMAIL_HOST_PASSWORD = '<IAM Access password>'
	EMAIL_USE_TLS = True
	DEFAULT_FROM_EMAIL = '<email to send from>'


