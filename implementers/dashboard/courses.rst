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

.. note::
	This is deprecated (as of server version 0.12.11) and should no longer be
	necessary to use this process. You can now assign multiple managers to
	courses (see: :ref:`permission-user-add-republish`)

When a course is first published, the user publishing the course is the owner of
this course, and only they can re-publish the course. If a different user needs
to publish the course, then the course ownership will need to be changed.

#. From the menu bar, select 'Admin' > 'Django Admin'
#. Select 'Courses' under the 'Oppia' section
#. Browse or search for the course and select it
#. Change the `user` to the new owner
#. Click save


Publish a draft course
-----------------------

To publish a course that's currently 'draft', republish the course from Moodle, 
selecting the "Live" option on export.

Alternatively (though deprecated):

#. From the menu bar, select 'Admin' > 'Django Admin'
#. Select 'Courses' under the 'Oppia' section
#. Browse or search for the course and select it
#. Untick the 'is draft' checkbox
#. Click save


Download course package
-------------------------

#. From the menu bar, select 'Courses'
#. Browse to the relevant course row
#. On the right hand side of the row, click 'download course'

Archive a course
-----------------

#. From the menu bar, select 'Admin' > 'Django Admin'
#. Select 'Courses' under the 'Oppia' section
#. Browse or search for the course and click on its link to edit it 
#. Tick the 'is archived' checkbox
#. Click save

Delete a course
-----------------

.. warning::
	Deleting a course will remove all its activity logs, learner progress and
	quiz scores. Most likely archiving a course is more appropriate
	
#. From the menu bar, select 'Admin' > 'Django Admin'
#. Select 'Courses' under the 'Oppia' section
#. Browse or search for the course and click on its link to edit it 
#. In the bottom left, click on 'Delete'
#. You will be asked to confirm deletion of the course