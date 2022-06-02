Course Statuses
=================

Draft
---------

*Designed for testing a course before being made available to users.*

Only users with Admin/Staff permissions, or those specifically with course 
viewer permissions for the course will be able to download this course to the
app.


Live
---------

*Designed for releasing a course to all users.*

All users will be able to download this course in the app.


New downloads disabled
-----------------------

*Designed for making courses unavailable to new users*

Users who already have the course installed can continue to use the course as
normal, however new users will not be able to download the course.

Read only
-----------------------

*Designed so users can only view course content*

Users who already have the course installed can continue to use it, although
they will not be able to access/view any of the quiz or feedback activities.
New users will not be able to download the course.

Archived
----------

*Designed for courses which are no longer in use.*

No users will be able to download this in the app (including Admin/staff users)


Deleted
---------

Not strictly a status, as this means that the course has been deleted from the
OppiaMobile server. Archiving a course is usually much more appropriate.

Changing a course status
---------------------------

If a course is status is changed, then this will affect who can access it in 
the app. 

If a course becomes newly available to a user (eg moving from draft to live),
they will get notified in the app that a new course is available for them to
download.
 
If a users has a course on their app and they no longer have access to this
course (due to change in status, eg live to archived), they will no longer be
able to access the course in the app, they will get a message that it should be
deleted from their app.

Status functionalities
-------------------------

App
~~~

.. raw:: html
   :file: status-app.html
   
Server Dashboard
~~~~~~~~~~~~~~~~

.. raw:: html
   :file: status-server.html

.. raw:: html
   :file: status-key.html
   
Notes
~~~~~

a. Not applicable as courses with this status can't be updated
b. Not applicable as learners cannot download a course with this status, or
   will be flagged as to delete if changed to this status
c. Course will be deleted from the app if it is updated to have one of these
   statuses
d. Only for learners who already have the course installed
e. If the course is moved from another status to one of these statues, then the
   course will get flagged as to delete, but depending on connectivity this
   might not happen instantly. So any pending activity will still get added to
   the aggregated stats until the course is removed form the users device.
f. Changing the gamification is a change in the course, requiring an update to
   the course in the app, so needs to be disabled if updating courses is
   disabled 
g. Since assumes that the course has previously been live, so users could have
   activity in this
h. Users will not be able to access the quizzes or feedback, but they will be
   able to review their previous attempts/responses
i. Since the quizzes and feedback aren't accessible they won't create any new 
   activity logs/trackers for these
   
Restrictions on statuses when republishing from Moodle Block
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The Moodle Oppia Export Block only allows courses to be pushed in either draft or live status, and so if a course has
been marked on the Oppia server as having (eg) read-only status, you will be prevented from re-publishing from the
Moodle Oppia Export Block. The combination of what status you can re-publish vs what status the course has on the server
is as follows:

.. raw:: html
   :file: status-republishing.html 
   
The rationale for this is that new-download-disabled, read-only and archive statuses are for course that have previously
been live but are no longer being updated. For read-only and new-download-disabled, new users will not be able to
install these and archived course will get marked as to be removed from users devices.

Courses which have a status which is not draft or live, have been explicitly marked as such on the server, so should not
be updated from Moodle. If these course really do need to be updated and republished, then the status on the server
should be moved back to draft or live first.
   