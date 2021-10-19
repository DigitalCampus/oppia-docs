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

Testing this is more tricky since by default a developer would need to wait at 
least a day (in the case of daily reminders), to see the reminders appearing. So
to automatically trigger notifications when the app is started you can make a 
small (temporary) change in the code for testing this:

To be completed