Using Cohorts (Groups)
=======================

A cohort is a collection of courses, student users and teacher users, which
allows the teacher users access to the server dashboard to view the activity of
the student users for the specific courses.

Example Use Cases
-------------------

* A health worker supervisor needs to view the course activity for all courses
  for the health workers they supervise. In this case, set up a cohort with the
  supervisor as the `teacher`, the health workers as the `students` and all the
  courses.
* A course mentor needs to view the course activity for all the students in just 
  the courses they are mentoring. In this case, set up a cohort with the mentor 
  as the `teacher`, all the students and the specific courses they need to 
  mentor.
* A regional health manager needs to view all the activity for all courses for
  all the health workers in their region. In this case, set up a cohort with the
  manager as the `teacher`, all the courses, and the health workers (`students`)
  the manager manages.


How to create/manage cohorts
------------------------------

Cohorts can be created from the Oppia server dashboard (select `cohorts` in the side menu), however only admin and staff
users are able to create cohorts.

.. toctree::
   :maxdepth: 2
   
   /implementers/dashboard/cohorts
   
Cohorts based on user profile fields
-------------------------------------

You can set up criteria to add users automatically to a particular cohort, instead of needing to add manually
one-by-one, see:  

.. toctree::
   :maxdepth: 2
   
   custom_criteria


What can teacher view
-------------------------

When a teacher logs into the Oppia dashboard, they will only be able to see the
course/user activity for the cohorts they have been assigned as a teacher.

For example, if a cohort has `teacher A` is the teacher, `course 1` and 
`course 2` as courses, and `user x` and `user y` as the students, the teacher 
will only see the activity for those courses for those users. If `user z` is 
also participating in `course 1`, the teacher will not see any of `user z's` 
activity.

Additional info on teacher permissions can be found at: 
:doc:`/implementers/permissions/server`


Additional notes
-------------------

* To assign users (teachers or students) and courses to a cohort, these users
  and courses need to exist on the server first. I.e. you can't add users or 
  courses to a cohort in preparation for users registering, or a course being 
  uploaded at a later date.
* You can add start and end dates to a cohort, however this is just for 
  information purposes (eg a class of 2020, a class of 2021), it doesn't change
  the access the teachers or students have to the course.
* Oppia users can be both teachers and students, for example, they might be a
  student in one cohort, but be a teacher in another.
