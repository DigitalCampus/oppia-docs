Restricting course access to specific cohorts
===============================================

Cohorts can be used to restrict access to some courses to a specific set of
users. To use this functionality, an admin or a staff user has to do the
following:

* Create a cohort with the course (or courses) that wants to apply restricted access
* Add in this cohort the users that will have access to this course
* Edit the course settings from the "Courses" section, and check the field "Restricted" for it

If a course is in multiple cohorts, then it will be available to all users in
any of the cohorts, independently of the role within the cohort, but no other
users. This applies both to the app and the server dashboard.


How course restrictions affect app functionalities
-----------------------------------------------------

The most obvious functionality for courses with restricted access from within
the app is that new learners that don't belong to the course's cohort do not
see the course listed to download.

If a cohort is updated (users or courses are added/removed), a new cohort
is created or the restricted/unrestricted property of the course is updated,
the next time the app updates the course statuses the changes implied by the
new scenario will be reflected, i.e. the users logged-in in the app will
gain or lose access to those courses.

If a course is restricted to a user (whether it is because the user downloaded
it in the app before it became restricted or because there are multiple users
logged-in in the device and not all of them have access to that course), the
following applies:

* The course won't appear under the course list in the app
* The user won't receive notifications for course updates
* The course contents won't appear under search results
* The course won't be accessible for that user through weblinks
