Rapid Deployment of OppiaMobile Implementation
====================================================

This page describes the processes for a rapid set up and deployment of 
OppiaMobile

Prerequisites
-----------------

* A technical person/team with experience in deploying OppiaMobile
* An AWS account, or admin (root) access to a locally hosted server
* A Google Play developer account, preferably a Ministry or government account



Oppia Server
----------------

* Create a clone/fork of the OppiaMobile core server code (from: 
  https://github.com/DigitalCampus/django-oppia)
* Either:

  #. set up a new local server for Oppia (see: :ref:`manualinstall`)
  #. launch and instance of the Oppia AWS server (see: :ref:`aws`)

* Set up a domain name to point to this servers IP address
* The server theme can be updated, but likely this can be dealt with later.


Oppia App
------------

* Create a clone/fork of the OppiaMobile core app code (from:
  https://github.com/DigitalCampus/oppia-mobile-android)
* Import into Android Studio
* Follow the instructions here to update the app - :ref:`custom_app`
* Submit the app to the Google Play store


Content
-------------

* Preferably any new content should be written and developed with mobile
  adaptation in mind from the start. Otherwise the content adaptation will take
  much longer.
* Ensure a full review of the content takes place on an actual device

Deployment to users
-------------------------

* For quickest deployment, the users can be pregistered in the app, and the
  content pre-loaded, although this is not possible for users who might be
  remotely installing the app themselves 
* Adapt or re-use the :ref:`introtraining`

