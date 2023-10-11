Upgrading Oppia server Operating System
=========================================

For the OppiaMobile servers that Digital Campus runs, and also the Amazon Machine Image (AMI) we maintain, we use Ubuntu
server (LTS version). The OS version we currently support is that one the AMI currently uses, using other versions of
Ubuntu may or may not work.

For the versions of MySQL, Apache and other system packages, we use the versions that are maintained by the Ubuntu
package manager for the Ubuntu version.

.. note::

	We don't advise upgrading a live OppiaMobile server to a Ubuntu version newer than the version the AMI is running,
	since usually the default version of Python for each Ubuntu OS is updated, which may require updates in the Oppia
	server code.

To upgrade your OppiaMoile server to the next supported Ubuntu server use the usual Ubuntu distribution upgrade process.

After upgrading Ubuntu, very likely you will need to rebuild the Python virtual environment, by deleting the old one and
re-installing it and the required packages:  

* ``$ sudo rm -r env``
* ``$ virtualenv env``
* ``$ source env/bin/activate``
* ``(env)$ pip install -r django-oppia/requirements.py``

You will also need to update the Apache site config for any updated Python version that is used, updating the paths for
``WSGIDaemonProcess`` and ``LoadModule wsgi_module`` (run ``mod_wsgi-express module-config`` to get the
updated wsgi_module path)
