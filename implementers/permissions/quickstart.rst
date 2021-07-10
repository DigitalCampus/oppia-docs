Permissions for Course Development - Quick Start
=====================================================

An overview of the permissions needed in Moodle and on the Oppia server for 
content creators to publish and review their courses from Moodle to the Oppia 
app.

Permissions in Moodle
----------------------

The content creator will need to have either/both:

* teacher permissions in the course/s they need to update (in the case of
  existing courses)
* course creator permissions in the category they are going to create courses 
  in (in the case of creating new courses)


It shouldn't be necessary for the content creator to need full admin permissons
in Moodle. You can find more information on the Moodle roles and permissions 
system here: https://docs.moodle.org/en/Roles_and_permissions 


Publishing/Pushing a new course to an Oppia server
----------------------------------------------------

If the content creator is publishing/pushing a new course to the Oppia server 
(i.e. one that doesn't yet exist on the specific Oppia server), then the course 
creator will need either:

* ``can upload`` permission in their user profile (see: 
  :ref:`permission-user-upload`)
* staff or admin permissions (see: :ref:`permission-user-admin` and 
  :ref:`permission-user-staff`)


Updating a course on an Oppia server
---------------------------------------

To update a course, the content creator will need to have the permissions above
for publishing a new course.

* If the course being updated is one that the content creator had already 
  published, then they don't need any extra permissions.
* If the course being updated is one that someone else has previously published,
  the content creator will need specific permission to publish this course (see: 
  :ref:`permission-user-add-republish`)


Draft vs Live Courses
-------------------------

When published to the Oppia server, draft and live courses are treated as 
independent courses, so you might find you need to give permissions for each. 

For example: If a course has been published live by another user, but there 
isn't a draft for it, then the content creator will be able to publish a new 
draft version with just the new course permissions. But they will need the 
update permissions to publish the live version.

In this way you could have content creators who are able to push changes to the 
draft version, but different users being able to finally publish as live.

Staging vs Live Servers
-------------------------

If you have separate staging and live Oppia servers, then these are independent 
instances of Oppia, so permissions need to be set up separately on each instance.

You might also want to have different permissions for different users on staging 
vs live servers.


