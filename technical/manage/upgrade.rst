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

Update to a specific version number
----------------------------------------------

If you prefer to upgrade to a more recent version, but not necessarily the absolute latest, you can upgrade to a 
specific version:

#. Move to the django-oppia directory: ``$ cd /home/oppiamobile/django-oppia/``
#. Checkout the specific version (in this instance 0.14.2): ``$ sudo git checkout v0.14.2-release``

.. note::
    Each server release is tagged in the format vX.Y.Z-release, so you can specify which version you'd like to upgrade
    to.
    
.. warning::
    It is strongly advised that you do not try to downgrade as you will likely run into inconsistencies in the database,
    both data and structure, that can be very difficult to resolve.

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

* v0.12.2 - :ref:`serverv0.12.2_upgrade_extras` - can be updated before or after other upgrade steps
* v0.12.3 - :ref:`serverv0.12.3_upgrade_extras` - can be updated before or after other upgrade steps
* v0.12.19 - :ref:`serverv0.12.19_upgrade_extras` - can be updated before or after other upgrade steps
* v0.12.22 - :ref:`serverv0.12.22_upgrade_extras1` and :ref:`serverv0.12.22_upgrade_extras2` - should be updated after
  other upgrade steps
* v0.12.24 - :ref:`serverv0.12.24_upgrade_extras` - should be updated before other upgrade steps
* v0.13.0 - :ref:`serverv0.13.0_upgrade_extras` - should be updated before other upgrade steps
* v0.14.0 - :ref:`serverv0.14.0_upgrade_extras` - can be updated before or after other upgrade steps
