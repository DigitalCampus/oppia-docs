User and Permissions Management
===================================

Add a new user
----------------

Either:

#. Just register a new user (using the 'Register' link in the menu bar)

Or:

#. From the menu bar, select 'Admin' > 'Django Admin'
#. Select 'Users' under the 'Authentication and Authorization' section
#. Select 'Add a new user' and complete the form

Bulk upload users
--------------------

#. From the menu bar, select 'Admin' > 'Upload users'
#. Prepare a CSV file with all the user info. You can create a CSV file in Excel. 
   Note that the column names are case sensitive and must be written exactly.
#. Upload the file
#. After processing you'll receive a report detailing the results

Remove a user
---------------

.. warning::
	Removing a user will delete all their activity logs and course progress. If you 
	would like to stop a user from accessing Oppia, but without deleting all their 
	activity logs, then use 'Block a user account' instead.
	
#. From the menu bar, select 'Admin' > 'Django Admin'
#. Select 'Users' under the 'Authentication and Authorization' section
#. Browse or search for the user and select
#. In the bottom left, click on 'Delete'
#. You will be asked to confirm deletion of the user account
	
Block a user account
---------------------

#. From the menu bar, select 'Admin' > 'Django Admin'
#. Select 'Users' under the 'Authentication and Authorization' section
#. Browse or search for the user and select
#. Untick the 'active' checkbox
#. Click on the save button (bottom right)

You can unblock a user account in a similar way - just tick the 'active' 
checkbox instead.

Reset user password
-----------------------

.. note::
    There is no way to find out what the original password was, as the passwords
    are stored in an encrypted format.
    
#. From the menu bar, select 'Admin' > 'Django Admin'
#. Select 'Users' under the 'Authentication and Authorization' section
#. Browse or search for the user and select
#. Under the password field, follow the link and instructions to reset the password

.. _permission-user-admin:

Add/remove admin access permission
------------------------------------

.. warning::
	Admin accounts have permissions to add, edit and delete any or all of the
	data stored, as well as create other Admin user accounts. Admin permissions
	should only be given to users who really need it, and consider giving staff
	status instead.
	
#. From the menu bar, select 'Admin' > 'Django Admin'
#. Select 'Users' under the 'Authentication and Authorization' section
#. Browse or search for the user and select
#. Tick/untick the 'superuser status' checkbox
#. Click on the save button (bottom right)


.. _permission-user-staff:

Add/remove staff access permission
-----------------------------------

#. From the menu bar, select 'Admin' > 'Django Admin'
#. Select 'Users' under the 'Authentication and Authorization' section
#. Browse or search for the user and select
#. Tick/untick the 'staff status' checkbox
#. Click on the save button (bottom right)

.. _permission-user-upload:

Add/remove permission to upload courses
------------------------------------------

#. From the menu bar, select 'Admin' > 'Django Admin'
#. Select 'User Profiles' under the 'Oppia' section
#. Browse or search for the user and select
#. Tick/untick the 'Can upload' checkbox
#. Click on the save button (bottom right)

.. _permission-user-add-view-draft:

Add permission to view draft course
---------------------------------------------

#. From the menu bar, select 'Admin' > 'Django Admin'
#. Select 'Course Permissions' under the 'Oppia' section
#. Select 'Add course permission' from the top right
#. Select the user you wish to give permission to, and the specific course
#. Select 'Viewer' as the role
#. Click on the save button (bottom right)

.. _permission-user-remove-view-draft:

Remove permission to view draft course
---------------------------------------------

#. From the menu bar, select 'Admin' > 'Django Admin'
#. Select 'Course Permissions' under the 'Oppia' section
#. Browse/Search to find the user and course you'd like to remove the permission
   for and select this row, so you see the entry edit field
#. Click on the delete button (bottom left) and confirm


.. _permission-user-add-republish:

Add permission to republish a course
---------------------------------------------

#. From the menu bar, select 'Admin' > 'Django Admin'
#. Select 'Course Permissions' under the 'Oppia' section
#. Select 'Add course permission' from the top right
#. Select the user you wish to give permission to, and the specific course
#. Select 'Manager' as the role
#. Click on the save button (bottom right)

.. _permission-user-remove-republish:

Remove permission to republish a course
---------------------------------------------

#. From the menu bar, select 'Admin' > 'Django Admin'
#. Select 'Course Permissions' under the 'Oppia' section
#. Browse/Search to find the user and course you'd like to remove the permission
   for and select this row, so you see the entry edit field
#. Click on the delete button (bottom left) and confirm

.. _permission-user-exclude-reporting:

Exclude a user from reporting analytics
---------------------------------------------

.. note::
    The exclusion (or re-inclusion) of a users activity only takes effect on
    the activity records that arrive at the server after this flag has been
    changed. I.e. it is not automatically applied retrospectively.
    To apply changes retrospectively, the 
    :ref:`update_summaries --fromstart <management_command_update_summaries>`
    command must be run.

#. From the menu bar, select 'Admin' > 'Django Admin'
#. Select 'User profiles' from the 'Profile' section
#. Browse/Search to find the user you'd like to exclude, and click on their 
   username, so you see the record edit form
#. Tick the 'Exclude from reporting' checkbox then save

Similarly, to re-include a user, untick this checkbox and save.


    