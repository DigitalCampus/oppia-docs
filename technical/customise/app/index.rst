.. _custom_app:

OppiaMobile Android App Customisation
=======================================

This section describes some of the basic customisations you may want to make when
implementing your own version of the OppiaMobile learning platform. Here we 
describe some of the more common requests for basic customisations, however 
since the code is open source, you are, of course, free to make any 
customisations you like.

Prerequisites
--------------
Before being able to create your own version of the OppiaMobile app, you should 
have an understanding of:

* Using Android Studio for development
* Basic understanding of the Android Java framework
* How to use GitHub for source code management

If you are completely new to any of the above, here are a few links to help get 
you started:

* Android development environment - https://developer.android.com/
* Android app development - getting started - http://www.vogella.com/android.html
* Git - http://git-scm.com/
* GitHub training (https://help.github.com/) and help (https://help.github.com/) 


Getting Started
---------------
* Set up your development environment
* Create a fork of the `oppia-mobile-android` repository in GitHub
* Clone your new GitHub repository to your machine
* Create a project in Android Studio connected to this repository
* Ensure that you are able to compile and run (either on your physical Android 
  phone or on an Android Virtual Device)

.. note::
    If you are running an Android Virtual Device (AVD) connected with a local server,
    the IP provided by it will not work directly in your app because this means it is pointing to the
    localhost of the AVD itself and not to your PC hosting the server.
    To solve that, `Android provides a special IP address <https://developer.android.com/studio/run/emulator-networking>`_ which points to your PC localhost
    in the corresponding port. This is the address you should configure in your app: ``http://10.0.2.2:<port>``
  
Please ensure that you are able to compile and run the core version of the app
before you start to make any changes to the code.

Configuring your own version of the app
----------------------------------------

.. toctree::
   	:maxdepth: 1
   	
   	configure 
   	settings
   	theme
   	preloading




