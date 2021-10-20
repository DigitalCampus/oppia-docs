Testing in-app Notifications
=============================

There are 2 types of in-app notifications:

For course updates and new courses
------------------------------------------------------

Notifications are sent to users when there are new courses and updated course. 
These notifications will only appear once although for updated courses the user
will be asked to update the course when they try to access the course.

For testing this, you can publish new/updated courses to your Oppia server. The 
notifications may not be instant, but will appear soon, or if the app is
restarted.

Reminders for users to complete courses
------------------------------------------

Notifications can be configured to remind users to complete their unfinished
courses. These notifications depend on the default notifications (set up in 
:ref:`notification_settings`), and then the users preferences for the reminder
days and times.

For testing this, without needing to wait a full day (or week) for the 
notification to appear:

#. Install a course on your device that is not yet completed
#. Reset the activity for this course (on the main app screen, long press on the 
   course, and select ``reset``), as this will remove all your course activity 
   from the app (but not the server)
#. Then you can set the reminder time to be a few minutes in the future to check
   that it appears as expected
   
.. note::

   These notifications might get shown a few minutes after the set time, eg if 
   set to 11:00, the notification might actually appear at 11:04. This is 
   because Android might process the notification slightly later if there are 
   other processes that are still running, this helps Android to optimise 
   performance and save battery.
   
For developers, when you build a debug version of the app (as you would when 
compiling and installing the app from Android studio to a connected device or 
AVD), in the settings (under the notifications section), you will see an 
additional ``Reminders Log``. On opening this you can see the history of when 
the notifications settings have been changed, when the notification was 
processed and whether it was actually displayed or not. This can assist with 
debugging if you make changes to the code or settings for this.
   