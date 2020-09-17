Updating Content using Oppia Export Block below v1.1.1
=========================================================

.. note::
	if you are using block version v1.1.1 or above, please refer to: 
	:doc:`updating-new-block`

For updating a course once it has been made live, there are 3 potential options,
each with their own pros/cons and considerations:

Option A: Edit in-place in Moodle
-----------------------------------

You can just edit the original version of the course directly in Moodle, then:

#. Export the course via the Oppia export block
#. Do not publish the course to the Oppia server, even as a draft version
#. Instead, directly download the course zip file, and 'sideload' this onto
   your device (see: :ref:`sideloadcontent`)


Pros
~~~~~

* This will preserve any user progress for unchanged activities when the course
  is finally made live.
* Reviewers/Testers for the course do not need to be given staff/admin
  permissions on the Oppia server.

Cons
~~~~~

* The course zip files need to be shared 'manually' to those who will be
  reviewing/testing.
* If any urgent changes are needed to the content, before the final version is
  complete, this will not be possible without pushing out the unfinished 
  version of the course.

Considerations
~~~~~~~~~~~~~~~~

* In this option, publishing the course as a draft version will remove the 
  option for learners to download the original/currently live version of the
  course. 


Option B: Clone the course in Moodle
--------------------------------------

The process for this option would be:

#. Create a copy of the course in Moodle (with a new course shortname, eg
   'course-v2')
#. Edit the new version of the course
#. Export and publish this new version as a draft to the Oppia server
#. Reviewers/Testers (with staff or admin permissions) will be able to directly
   download the new version into their Oppia app (without the new for 
   'sideloading'). Although the sideloading option is still a possibility if 
   you don't want to give all the reviewers staff/admin permissions on the
   server
#. Once the new version is ready, update the shortname of the old version, eg 
   'course-v1', then update the shortname of the new version to be the original
#. The course can then be published live via the Oppia export block


Pros
~~~~~

* Interim/urgent updates can be made to the original version of the course.
* No need to distribute the course zip file manually and ask reviewers/testers
  to sideload

Cons
~~~~~

* When published live, all activities will appear to the user as new activities,
  even those that haven't been updated (since the id numbers in Moodle will
  have changed)
* Reviewers and testers need to have staff/admin permissions 


Option C: Edit in place and republish live (NOT recommended)
---------------------------------------------------------------

Of course, you can just make edits to the current version of the course and
republish live directly. 

If the edits are very minor (eg correcting typos/mistakes etc), and so don't
need a full review/test, then likely this will be no problem.

If the course has more substantial updates, that need review and testing first,
then this approach is not recommended.