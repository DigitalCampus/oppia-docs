Course Management
=====================


Add a new course
-------------------

.. note::
   Usually courses would be added directly from Moodle during the export process
   
   
#. From the menu bar, select 'Upload'
#. Select the course zip file that you exported from Moodle
#. Click on upload
#. Add or update the course tags and other information
#. Click save   


View all courses
-------------------

#. From the menu bar, select 'Courses'

View courses for specific tag
---------------------------------

#. From the menu bar, select 'Courses'
#. From the drop down list of tags at the top of the page, select the relevant tag
#. The page will refresh and show just the courses for the selected tag

Update course information (tags etc)
---------------------------------------

Currently this should be done during the course export process in Moodle.

.. _permission-course-ownership:

Change the ownership of a course
-----------------------------------

When a course is first published, the user publishing the course is the owner of this course, and only they can re-publish the course.
If a different user needs to publish the course, then the course ownership will need to be changed.

#. From the menu bar, select 'Admin' > 'Django Admin'
#. Select 'Courses' under the 'Oppia' section
#. Browse or search for the course and select it
#. Change the `user` to the new owner
#. Click save



Publish a draft course
-----------------------

To publish a course that's currently listed as 'draft', you can either republish the course from Moodle, unticking the 
'is draft' option, or follow these steps:

#. From the menu bar, select 'Admin' > 'Django Admin'
#. Select 'Courses' under the 'Oppia' section
#. Browse or search for the course and select it
#. Untick the 'is draft' checkbox
#. Click save

Similarly you move a course back to being a draft by ticking the 'is draft' option.

Download course package
-------------------------

#. From the menu bar, select 'Courses'
#. Browse to the relevant course row
#. On the right hand side of the row, click 'download course'

Archive a course
-----------------

.. note::
	Archived courses are no longer available for anyone to download, though users with 
	the course installed in their Oppia app will still be able to use the course as normal.

#. From the menu bar, select 'Admin' > 'Django Admin'
#. Select 'Courses' under the 'Oppia' section
#. Browse or search for the course and select it
#. Tick the 'is archived' checkbox
#. Click save

Delete a course
-----------------

.. warning::
	Deleting a course will remove all its activity logs, learner progress and quiz scores. If 
	you just want to make a course unavailable for download, then use 'Archive a course' instead.
	
.. note::
	Deleted courses will (obviously) no longer be available for download. Though users with the 
	course installed in their Oppia app will still be able to use the course, however no points, 
	activity, quiz scores will be recorded by the server.

#. From the menu bar, select 'Admin' > 'Django Admin'
#. Select 'Courses' under the 'Oppia' section
#. Browse or search for the course and select it
#. In the bottom left, click on 'Delete'
#. You will be asked to confirm deletion of the course