OppiaMobile App User Guide
=============================

This is a template user guide, based on the core Oppia app, which can be
adapted/edited to fit a particular implementation.


Introduction 
--------------

OppiaMobile is a mobile learning platform specifically designed for learners in
low connectivity environments. Course content can be accessed even when you are
offline, although initially you will need an internet connection to install the
app, register and get the courses.

Installing the app
-------------------

You can download the OppiaMobile app from the Google Play Store at:
https://play.google.com/store/apps/details?id=org.digitalcampus.mobile.learning

When you first open the OppiaMobile app, you will be asked to confirm the
following permissions:

* Read phone state and identity - this is to check the internet connectivity
  status
* Read and modify contents of the SD card - this is to be able to store the
  course contents locally on your phone

.. image:: images/permissions.png
    :align: center
    :width: 250

Please allow the OppiaMobile app access to both of these permissions, they are
required to ensure the app can function correctly.

Registering or Logging In
----------------------------

.. image:: images/login_register.png
    :align: center
    :width: 250

To use OppiaMobile you will need to either login or register.

If you already have an account, or a username/password has been given to you,
then please just press the button to login.

.. image:: images/login.png
    :align: center
    :width: 250

If you do not have an account, then please press the register button and 
complete the required information to create an account. The exact information
you need to register will depend on the specific implementation, and the
information they require for you to register.

.. image:: images/register.png
    :align: center
    :width: 250



Installing Courses 
-------------------------------

After logging in or registering, you will then need to download the courses to
access. When you have no courses installed, you will see this screen:

.. image:: images/home_no_courses.png
    :align: center
    :width: 250

Click on the ``manage courses`` button to go through and select the courses you
would like to download. Course are divided into categories, so you can select
the appropriate category:

.. image:: images/categories.png
    :align: center
    :width: 250
    
For example, selecting the ``OpenWASH - Ethiopia`` category, will then show you
the courses available:

.. image:: images/wash_category.png
    :align: center
    :width: 250
    
You can then download each course separately, by clicking on the download icon
next to each course. Alternatively you can select all the courses to download 
from the menu button in the top right of the screen:

.. image:: images/download_all_1.png
    :align: center
    :width: 250
    
.. image:: images/download_all_2.png
    :align: center
    :width: 250

Even after you have downloaded some initial courses, you can always get back to
install more. From the main Oppia app page, click on the sidebar menu:

.. image:: images/download_new_1.png
    :align: center
    :width: 250

Then select ``Download courses``:

.. image:: images/download_new_2.png
    :align: center
    :width: 250

Then you will taken back to the course categories page to select the courses you
would like to download.

 
Installing Media
-------------------

If the courses you have installed also have some media embedded (eg videos or
audio content), you will need to download these separately. On the Oppia 
homepage it will give you a notification if there are any missing media files
for the courses you have downloaded:

.. image:: images/download_media.png
    :align: center
    :width: 250
    
Click the ``Download`` button and follow the instructions to download any media
files that you do not already have installed.

Navigating Courses
---------------------

On the Oppia app homepage, you will see a list of all the courses you have
installed:

.. image:: images/home_courses.png
    :align: center
    :width: 250
    
Click on a course to enter it and start the activities, each course has an index
of all the sections and activities:

.. image:: images/course_index.png
    :align: center
    :width: 250


When you select an activity, the activty will load:

.. image:: images/course_activity.png
    :align: center
    :width: 250
    
You can swipe left/right to navigate through all the activities inside that 
section.

Some courses have a pre-test quiz that you will need to complete before you can
access the full course content.

Points and Badges
------------------

You will earn points and badges for taking part in activities and completing
courses.

Points are awarded based on your interaction with the course content, eg 
completing an activity or quiz.

Badges are awarded when you complete a course, this means completing every
activity, including watching all the course media content and passing every
quiz.

You will see the number of points and badges that you have been awarded in the 
menu bar.


Scorecard
----------

There are two scorecard formats in the Oppia app. One shows the progress overall
for all the courses that are installed. This can be accessed from the bottom 
menu bar on the app homepage:

.. image:: images/scorecard_general.png
    :align: center
    :width: 250

The second one shows more detailed scorecard for a particular course. This can
be accessed from the specific course index page and clicking on the scorecard
icon in the menu bar:

.. image:: images/scorecard_course.png
    :align: center
    :width: 250
    

Changing your preferences
---------------------------

You can change your preferences, for example the default text size, points
notifications etc from the main app settings screen. From the app homepage:

.. image:: images/settings_access1.png
    :align: center
    :width: 250
    
Then select ``Settings``:

.. image:: images/settings_access2.png
    :align: center
    :width: 250

You can then update the settings you would like to change:
    
.. image:: images/settings_home.png
    :align: center
    :width: 250

Course Updates
----------------

When courses that you have installed are updated, for example for new/updated 
content, you will be automatically notified in the standard Android home menu
bar, from the notification you can go directly to download the updated course.
Note that you will need to have regular internet connection to be able to
receive these notifications.

You can always check manually for course updates, and install additional
courses, by following the instructions above for downloading courses.

Help, Support and Feedback
----------------------------

In most cases, if you need help or support, then you should first contact your
project coordinator. They will try to help you, and if they are not sure, they
will raise the query with the OppiaMobile developer team.

