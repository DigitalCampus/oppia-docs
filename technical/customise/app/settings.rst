Settings and Defaults
========================

The OppiaMobile Android app makes use of the Android build system to define at compile time some of the settings for the 
project, so you don't need to modify any source code. This is done by reading a file in the root of the project called 
``oppia-default.properties`` and creating all the necessary BuildConfig values.

If you want to overwrite any of this settings, create a new file named ``custom.properties`` and define any value of the 
list below that you want to override. Note that you don't need to define all the values again, simply the ones you want 
to override, and the rest will use the default value.

**IMPORTANT**: The ``custom.properties`` file is ignored by Git in order to hide private configuration settings (like 
API keys), so any changes you make to it will not be visible in your repository. 

List of configurable values
---------------------------

.. _general_settings:

General settings
^^^^^^^^^^^^^^^^^
* ``ANALYTICS_LIBRARY`` (string): Defines the analytics/bug report library to use. If left empty or not present, no analytics will be tracked. Currently, Oppia supports two possible values (uppercase): ``MINT`` for **Splunk Mint**, ``COUNTLY`` for **Countly**.  
* ``COUNTLY_APP_KEY`` (string): the Countly API key to use for the bug/analytics reports
* ``COUNTLY_SERVER_URL`` (string): the URL for the Countly server instance to use for the bug/analytics reports
* ``MINT_API_KEY`` (string): the Splunk Mint API key to use for the crash reports
* ``OPPIA_SERVER_DEFAULT`` (string): the initial Oppia server URL. By default, the demo server ``https://demo.oppia-mobile.org/``
* ``OPPIA_SERVER_HOST`` (string): the server hostname, for the intent filter functionality (to be able to open links from external apps directly in the app). For example, if our server is ``https://demo.oppia-mobile.org/`` this config should be set to ``demo.oppia-mobile.org``
* ``SESSION_EXPIRATION_ENABLED`` (boolean): enable that the session of the current user expires after a certain inactivity time. False by default
* ``SESSION_EXPIRATION_TIMEOUT`` (int): seconds of inactivity to expire a user's session (only works if the previous one is set to true)
* ``OFFLINE_REGISTER_ENABLED`` (boolean): enable user to register an account even if offline. True by default.
* ``START_COURSEINDEX_COLLAPSED`` (boolean): show the course index with each section collapsed. False by default.
* ``SHOW_COURSE_DESCRIPTION`` (boolean): show the course index description in courses list. False by default.

Local admin settings (all false by default)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

These settings control the functionality of protecting different app actions by a local admin password, to control which
actions are allowed to a normal user without this password. Is an option available in the preferences screen of the app (disabled by default),
but by this values you can control which specific actions are controlled by the admin password.

* ``ADMIN_PROTECT_INITIAL_PASSWORD`` (boolean): the admin password to set initially (it can be changed later in the settings screen). If it is set,
  then the admin protection will be enabled from the start by this password.
* ``ADMIN_PROTECT_SETTINGS`` (boolean): protect settings screen by admin password. If this is set to `false`, a normal user will
  be able to access the preferences screen even if the admin initial password is set, but to change the admin protection and the admin password
  she would need to enter the current password first.
* ``ADMIN_PROTECT_COURSE_DELETE`` (boolean): protect course deletion by admin password
* ``ADMIN_PROTECT_COURSE_RESET`` (boolean): protect course reset by admin password
* ``ADMIN_PROTECT_COURSE_INSTALL`` (boolean): protect course installs by admin password
* ``ADMIN_PROTECT_COURSE_UPDATE`` (boolean): protect course update by admin password
* ``ADMIN_PROTECT_ACTIVITY_SYNC`` (boolean): protect synchronising activity by admin password
* ``ADMIN_PROTECT_ACTIVITY_EXPORT`` (boolean): protect exporting activity by admin password
* ``ADMIN_PASSWORD_OVERRIDE_VERSION`` (int): the ``versionCode`` number of the app in which the password should be overriden.

A situation may arise where the admin password set in the currently installed version needs to be
overriden by a new known one. Setting this value to the current version code number of the app will set the ``ADMIN_PROTECT_INITIAL_PASSWORD`` as
the current admin password the first time the app is initialized (as with the initial password, it can be changed later in the settings screen again).

Main menu configurations
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* ``MENU_ALLOW_MONITOR`` (boolean): show the "Monitor" option in the main menu
* ``MENU_ALLOW_SETTINGS`` (boolean): show the "Settings" option in the main menu
* ``MENU_ALLOW_COURSE_DOWNLOAD`` (boolean): show the "Install courses" option in the main menu
* ``MENU_ALLOW_SYNC`` (boolean): show the "Sync" option in the main menu
* ``MENU_ALLOW_LOGOUT`` (boolean): show the "Logout" option in the main menu
* ``MENU_ALLOW_DOWNLOAD`` (boolean): show the "Download" option in the main menu
* ``MENU_ALLOW_LANGUAGE`` (boolean): show the "Language" option in the main menu
* ``DOWNLOAD_COURSES_DISPLAY`` (int): max number of courses installed in which the "download more courses" button still appears in the main activity. By default, just one.


Metadata collection
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The app saves a set of metadata additional information for every activity tracker log. The metadata to include in
each tracker can be configured in the server, so the first time a user logs in or register this configuration is fetched
and the app only saves the expected metadata for that specific server.

There can be cases where this configuration is not fetched from the server, for example in the case of a preloaded account
in the device or an offline registered user. With the following settings we can control which metadata values should be
included by default in the tracker logs:

* ``METADATA_INCLUDE_NETWORK`` (boolean): Include in the tracker metadata the current network operator name
* ``METADATA_INCLUDE_DEVICE_ID`` (boolean): Include in the tracker metadata the unique device identifier
* ``METADATA_INCLUDE_SIM_SERIAL`` (boolean): Include in the tracker metadata the SIM serial number
* ``METADATA_INCLUDE_WIFI_ON`` (boolean): Include in the tracker metadata if the device is currently connected to a WiFi network
* ``METADATA_INCLUDE_NETWORK_CONNECTED`` (boolean): Include in the tracker if the device has internet access
* ``METADATA_INCLUDE_BATTERY_LEVEL`` (boolean): Include in the tracker the device battery level


Gamification / Activity completion
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* ``GAMIFICATION_MEDIA_CRITERIA`` (string): the criteria that should be used for determining if a media activity has been completed and how to award points. Possible values:
    - ``threshold``: Default value. The media will be completed if the user watches the video for above a certain threshold (see next setting)
    - ``intervals``: Only mark the video as completed if it was watched for its full length. Points are awarded in intervals based in the percentage of video watched.

* ``GAMIFICATION_DEFAULT_MEDIA_THRESHOLD`` (int): if ``GAMIFICATION_MEDIA_CRITERIA`` is ``threshold``, then the minimum percent to consider if completed. ``80`` by default

* ``GAMIFICATION_MEDIA_SHOULD_REACH_END`` (boolean): Additionally to the specific criteria set to determine the activity media completion, the media playing must reach its end to consider it completed. By default, false.

* ``PAGE_COMPLETED_METHOD`` (string): the criteria that should be used for determining if a page activity has been completed based in the the time the user spent on it. Possible values:
    - ``TIME_SPENT``: Completed if the user stays in the activity longer than a fixed amount of time (defined in the ``PAGE_COMPLETED_TIME_SPENT`` setting, in seconds)
    - ``WPM``: The time the user has to stay in the activity is based on the activity's wordcount and the defined average reading speed.

* ``PAGE_COMPLETED_TIME_SPENT`` (int): Number of seconds the user has to stay in the activity to mark it as completed.

* ``PAGE_COMPLETED_WPM`` (int): WPM (words per minute) reading speed to calculate the time the user should spend in each activity for the WPM completion method. 

* ``GAMIFICATION_POINTS_ANIMATION`` (int): Defines the animation type if the previous setting ``Show gamification events`` is enabled. These are the different types of animation (default is number 3):
	1. Simple animation (circle rotation)
	2. Full animation (circle rotation and vertical translation)
	3. Full animation with sound

* ``DURATION_GAMIFICATION_POINTS_VIEW`` in seconds (int): Duration of the points awarded text after the configured animation (if any). ``2 seconds`` by default
