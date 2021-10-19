Server Settings
===============

There are several settings you can update to configure your OppiaMobile server.
Some settings need to be updated in the code and some can be configured in the 
Oppia database.


Code settings (settings_secret.py)
------------------------------------

To edit these settings you will need to edit your 
``/oppiamobile/settings_secret.py`` file, and
for them to take effect you will need to restart your web server.
 
 
``COURSE_UPLOAD_DIR``


Default `ROOT_DIR +'/upload'`

This is the path to where uploaded course will be saved.


``OPPIA_METADATA``


Default:

::

	{
	    'NETWORK': True,  
	    'DEVICE_ID': True,
	    'SIM_SERIAL': True,
	    'WIFI_ON': True,
	    'NETWORK_CONNECTED': True,
	    'BATTERY_LEVEL': True
	}

The defines the metadata info that is sent back from the app (included in each 
activity tracker response)


``BADGE_AWARDING_METHOD``

.. note::
   This is deprecated from server version 0.12.13 onwards. To change the badge
   award method this can now be done in the Oppia admin pages, see: 
   :doc:`../../../implementers/dashboard/gamification`


``OPPIA_VIDEO_FILE_TYPES``


Default: ``("video/m4v", "video/mp4", "video/3gp", "video/3gpp")``

List of the video file MIME types that will be accepted for upload to the server.

``OPPIA_AUDIO_FILE_TYPES``

Default: ``("audio/mpeg", "audio/amr", "audio/mp3")``

List of the audio file MIME types that will be accepted for upload to the server.


``API_LIMIT_PER_PAGE``

Default: ``0``

Defines how many results will be returned per page in the API. When set to 0, all results will be returned.


``MEDIA_PROCESSOR_PROGRAM``

Default: ``"ffprobe"``

``MEDIA_PROCESSOR_PROGRAM_PARAMS``


Default: ``""``



Database configurable settings
--------------------------------------

The following settings can be edited in the Django Admin pages (under 
``Settings > Settings``). The settings are divided into categories.

Analytics category
~~~~~~~~~~~~~~~~~~~

* ``OPPIA_GOOGLE_ANALYTICS_CODE`` (string, default: None) - Google Analytics 
  code, if enabled
* ``OPPIA_GOOGLE_ANALYTICS_DOMAIN`` (string, default: None) - Google Analytics 
  domain name, if enabled
* ``OPPIA_GOOGLE_ANALYTICS_ENABLED`` (bool, default: False) - 	Whether or not 
  Google Analytics is enabled

App category
~~~~~~~~~~~~~~~~~~~

* ``OPPIA_ANDROID_ON_GOOGLE_PLAY`` (bool, default: False) - Whether or not this 
  Oppia server has a specific app available on the Google Play Store
* ``OPPIA_ANDROID_PACKAGEID`` (string, default: 
  org.digitalcampus.mobile.learning) - The java package id of the specific app 
  on the Google Play Store

.. _certification-settings:

Certification category
~~~~~~~~~~~~~~~~~~~~~~~

* ``OPPIA_EMAIL_CERTIFICATES`` (bool, default: False) - Whether or not 
  certificates should be emailed to users

Gamification category
~~~~~~~~~~~~~~~~~~~~~~~

* ``OPPIA_BADGES_ENABLED`` (bool, default: True) - Whether or not badges are 
  enabled for this Oppia implementation
* ``OPPIA_BADGES_PERCENT_COMPLETED`` (int, default: 80) - If the badging is set 
  to all quizzes plus a percentage of all other activities, what will that 
  percentage be
* ``OPPIA_POINTS_ENABLED`` (bool, default: True) - Whether or not points are 
  enabled for this Oppia implementation
  
  
Server Registration category
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* ``OPPIA_SERVER_REGISTERED`` (bool, default: False) - Whether or not this 
  server is registered with https://implementations.oppia-mobile.org
  
All the other server registration settings are best edited directly from the 
main Oppia dashboard from <your-oppia-url>/serverregistration/
  

System category
~~~~~~~~~~~~~~~~~~~~~~~

These should not need to be edited (unless you are very sure), as they are 
internal for the Oppia cron tasks.

.. _system-config-settings:

System Configuration category
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* ``MAX_UPLOAD_SIZE`` (int, default: 5242880, 5Mb) - The maximum upload size,
  in bytes, of course files that will be allowed
* ``OPPIA_ALLOW_PROFILE_EDITING`` (bool, default: True) - Whether or not users 
  can edit their user profile from the server dashboard. Note that even if this
  is set to False, users will still be able to edit their password.
* ``OPPIA_ALLOW_SELF_REGISTRATION`` (bool, default: True) - Whether or not this
  Oppia server allows users to self register
* ``OPPIA_DATA_RETENTION_YEARS`` (int, default: 7) - The number of years for 
  users data to be kept. Any users who have not logged in and not had any 
  tracker activity in this number of years will be removed from Oppia, along 
  with their activity data. Note that this removal will not happen 
  automatically, it needs the ``data_retention`` management command to be run 
  manually from the command line on the server
* ``OPPIA_HOSTNAME`` (string, default: None) - Domain/hostname for this Oppia 
  server
* ``OPPIA_SHOW_GRAVATARS`` (bool, default: True) - Whether or not to use 
  Gravatars for users' profile pictures

Visualisations category
~~~~~~~~~~~~~~~~~~~~~~~

* ``OPPIA_CARTODB_ACCOUNT`` (string, default: None) - Username for the CartoDB 
  account
* ``OPPIA_CARTODB_KEY`` (string, default: None) - CartoDB account API key
* ``OPPIA_IPSTACK_APIKEY`` (string, default: None) - IPStack API key
* ``OPPIA_MAP_VISUALISATION_ENABLED`` (bool, default: False) - Whether or not 
  the map visualization is enabled for this Oppia implementation

