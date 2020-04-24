Configuring your own version of the app
===========================================

Once you've cloned the OppiaMobile Android app code and check you can compile 
and run the app on your device, there are some changes you should make to the 
configuration.

The main reason to make these changes is so that you can:

* Submit your app to the Google Play Store - you won't be able to submit an 
  unchanged clone of the core version to Google Play as the package name is 
  already used.
* Receive automatic notifications of any errors your users may get when using 
  the app
* Automatically have the app connect to your OppiaMobile server, and override
  other default settings from the core version


Rename applicationId
---------------------------

Update the ``app/build.gradle`` changing the ``applicationId`` value to a new 
one, keeping with the 'reverse url' type notation, so for example, replace 
``org.digitalcampus.mobile.learning`` with ``org.myorgname.myproject.oppia``.

Create custom.properties file
-------------------------------

Follow the instructions in :doc:`./settings` to create a ``custom.properties``
file to override any default settings in the core Oppia, such as the server
connection url and error reporting API key.


App title and welcome message
------------------------------------

To update your app title and company/organisation name, open the 
``app/src/main/res/values/strings.xml`` file and edit the ``ENTITY`` strings 
for:

* appName
* companyName

You should also change these strings in the other language string files, eg
``app/src/main/res/values-fi/strings.xml``

For updating the welcome message, you'll need to update the strings for:

* ``fragment_welcome_title``
* ``fragment_welcome_desc`` 
* ``fragment_welcome_login_info`` 

App logo
---------------

To use a different logo for your app, place your app logo in the drawables 
folder and update the ``app_icon`` reference in the ``res/values/theme.xml`` file.

To create the drawable for the app icon, you can rely on the Image Asset Studio tool that comes bundled with Android Studio to generate all 
the necessary images in its density-specific folder. To use it, just select right-click in the `res` folder of your project 
and select **New** > **Image Asset**. It will help you to create a Material design style icon based on your own 
image, and to generate the drawable in all the needed resolutions.