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

* ``MINT_API_KEY`` (string): the Splunk Mint API key to use for the crash reports
* ``OPPIA_SERVER_DEFAULT`` (string): the initial Oppia server URL. By default, the demo server https://demo.oppia-mobile.org/
* ``SESSION_EXPIRATION_ENABLED`` (boolean): enable that the session of the current user expires after a certain inactivity time. False by default
* ``SESSION_EXPIRATION_TIMEOUT`` (int): seconds of inactivity to expire a user's session (only works if the previous one is set to true)
* ``OFFLINE_REGISTER_ENABLED`` (boolean): enable user to register an account even if offline. True by default

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
* ``METADATA_INCLUDE_GPS`` (boolean): Include in the tracker the GPS location of the device


Gamification
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- ``GAMIFICATION_MEDIA_CRITERIA`` (string): the criteria that should be used for determining if a media activity has been completed and how to award points. Possible values:
    - ``threshold``: Default value. The media will be completed if the user watches the video for above a certain threshold (see next setting)
    - ``intervals``: Only mark the video as completed if it was watched for its full length. Points are awarded in intervals based in the percentage of video watched.

- ``GAMIFICATION_DEFAULT_MEDIA_THRESHOLD`` (int): if ``GAMIFICATION_MEDIA_CRITERIA`` is ``threshold``, then the minimum percent to consider if completed. ``80`` by default

- ``GAMIFICATION_POINTS_ANIMATION`` (int): Defines the animation type if the previous setting ``Show gamification events`` is enabled. These are the different types of animation (default is number 3):
	1. Simple animation (circle rotation)
	2. Full animation (circle rotation and vertical translation)
	3. Full animation with sound

- ``DURATION_GAMIFICATION_POINTS_VIEW`` in seconds (int): Duration of the points awarded text after the configured animation (if any). ``2 seconds`` by default
