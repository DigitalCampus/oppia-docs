Updating Content
==================================


Whilst a course for an Oppia implementation is being developed, and before the
app in launched, course content can be updated and published to the server as
often as is necessary.

However, once a course has been launched, and is being used by learners,
publishing updates should be well planned and coordinated. Firstly to reduce
the burden and potential confusion to users for having a lot of small, regular
updates and secondly, to ensure a good review can be made of the content before
it is made live for learners.

For testing updates to a live course, there are several options:

Option 1: Publish as draft/test course
----------------------------------------

When you are exporting from Moodle, you can specify if the course is a
draft/testing version or a live version.

If draft/test is selected the course shortname will automatically have "-draft"
appended to it and be pushed as a draft course to the Oppia server.

In this way, you're able to push an updated draft/test version of a course that
is already live to users, without overwriting the currently live version of the
course.

Once you are happy with all the updates, you can publish as a live course and
then it will update the live version on the Oppia server, and get pushed out to
users.

Option 2: Publish to a staging server
----------------------------------------

If you have a separate staging server for Oppia, you can use this to publish
your updated course to and test against this server.

For testing in the app, first log out (if you're already logged in and connected
to a live server), then change the server you're connecting to to be your
staging server.

Once you are happy with all the updates, you can publish as a live course on 
your live server, and get pushed out to users. Or, if you prefer, publish as a 
draft course to you live server (as option 1 above), for a final test, before 
making live.

Option 3: Combination of the above 2
-------------------------------------

You can publish a course as draft/testing or live to a staging server, although
as it's a staging server, it's not live to all your users (only your testers
connected to the staging server).

You might want to go through the process of publishing as draft and then live on
your staging server, to get familiar with the process (and how users are 
notified about updates), but without impacting your actual users.

How are users notified about course updates?
---------------------------------------------

[we are working on ways to improve the course notification process]

When a course is updated and published live, users will be notified on their
phone for courses that they already have installed (when they have an internet
connection available on their device). 

Users will not be notified about:

* updates to courses that they don't already have installed
* new courses
* courses that are no longer live 

Note that users are not forced to update courses, it is their decision when to
update a course (e.g. when they have access to wifi, or good mobile internet 
connection)

How to deal with courses that are no longer live
----------------------------------------------------

If a course is not being updated, but instead being removed, currently, users 
are not notified that a course is no longer in use.

The current/best approach will be to:

* Replace/update the course content to a single page to notify users they should 
  remove the course from their phones, and place the course in an 'archive'
  category.
* Then when users update the course, they will know that it is no longer valid.

Notes: 

* If the course is just archived from the server side, users will not get
  any notification, and they may continue to use it, not knowing that it is no
  longer in use. Although of course, new users will not be able to download this
  course.
* Courses cannot be 'remotely deleted' from a users device. Similarly with
  course updates, if will be up to the users to decide when to update a course
  on their device.

  
What happens to learner progress when a course is updated?
------------------------------------------------------------

When a course is updated, any activities that have been changed (in any way, 
from a minor typo, to a rewrite), the old version of the activity is 
essentially 'detached' from the new version of the course.

Any deleted activities are also just detached, and any new activities are just 
added. The tracker and quiz scores etc are retained.

From a user perspective on their device, when they download the new version:

* if they haven't yet completed the old version of the activity, there's no
  real difference to them
* if they completed the old version of the activity, but not completed the 
  course, the updated version of the activity will now show as no longer
  completed
* if they have already completed the course and got the badge, then they will
  keep the badge, but the updated version of the activity will now show as no
  longer completed
  

What happens if a user continues to use an old version of a course?
--------------------------------------------------------------------

If a user does not update (or remove) a course, they will be able to continue 
to use it on their devices as the version they have installed. They will still
get points for completing activities, but they will not be awarded a badge for
completing an old version of a course. Their usage information is still tracked
on the server.

