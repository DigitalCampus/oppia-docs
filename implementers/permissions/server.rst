OppiaMobile Server Permissions
================================

There are various permissions associated with users in OppiaMobile, some based 
on the default Django users system and others based on extra permissions the user
has been specifically given.

* **Admin User** - this is the standard Django superuser 
  (https://docs.djangoproject.com/en/2.2/topics/auth/default/) - a typical user 
  with this role would be a system/server administrator. Admin users are able to
  add/edit/delete any data directly from the Oppia Django Admin pages.
* **Staff** - this is the standard Django staff user 
  (https://docs.djangoproject.com/en/2.2/topics/auth/default/) - a typical user 
  would be a project manager/officer, college or ministry staff, essentially 
  users who need to access all the data/reports within the server, but not 
  necessarily responsible for the technical maintenance or server level admin.
  Staff users do not have any permissions to add/edit/delete data in the Oppia
  Django Admin pages.
* **Teachers/Students** - in Django permissions terms, both teachers and students 
  are standard users. The only difference between them is that a teacher has 
  been assigned the teacher status to a particular cohort of students. A cohort 
  is just a group of teachers and students assigned to a particular set of 
  courses. A user may have the role of teacher on one set of courses, but then 
  be a student on other courses.



Permissions on the OppiaMobile Server dashboard:
------------------------------------------------

.. raw:: html
   :file: permissions-server-table.html


Notes:

1. Staff are able to access the Django admin URL, however they do not have 
   permissions to view any of the data models or actual data through this
2. Any user (teacher or student) may be given permissions to upload courses by 
   changing the 'can upload' field in their UserProfile to be true.
3. Teachers may only view cohorts that they are teachers in.
4. Students may view their own activity within a cohort
5. Students and Teachers may view all the courses available on the server, 
   except those that are still in draft stage
6. A teacher may only view the activity for courses they are assigned to be 
   teachers on, and then only for the students in the cohorts they are teachers 
   in.
7. Students may see their own activity within a course or cohort - but not 
   anyone elses
8. Any user may be given Course viewer permissions to be able to view a specific 
   course that is currently draft
9. Any user may be given Course manager permissions to be able to update
   (republish) a course
10. There is a settings option to disable profile editing
