Database Summary Tables
=============================

Definitions:

* *attempted* - an activity that was tried, not necessarily that the activity was completed. Main difference here is
  for quizzes, if a user does a quiz, but does not pass, it will be included in attempted but not as completed.
* *submitted_date* - based on the date the activity log was submitted to the server, as recorded by the server date/time
* *attempted_date*/*tracker_date* - based on the date the activity occured on the device, recorded as the date/time the
  users device is set to

.. _summary_coursedailystats:

summary_coursedailystats
----------------------------

Overall summary of activity in particular course.

Columns:

* *id* - unique identifier for row in table
* *course_id* - id number of the course
* *day* - day/month/year, based on the tracker attempted date
* *type* - type of activity (eg page, quiz, media, download)
* *total* - total number of attempts for the defined type

Used for:

* Reports for course activity, downloads and searches
* Dashboard graphs for homepage and courses


.. _summary_usercoursedailysummary:

summary_usercoursedailysummary 
---------------------------------

Summary of activity and time spent by day, user, course and activity type

Columns:

* *id* - unique identifier for row in table
* *day* - day/month/year
* *type* - type of activity (eg page, quiz, media, download)
* *time_spent_submitted* - time spent for activity type based on submitted date
* *time_spent_tracked* - time spent for activity type based on tracked date
* *total_submitted* - number of attempts for activity type based on submitted date
* *total_tracked* -number of attempts for activity type based on tracked date
* *course_id* - id number of the course
* *user_id* - id number of the user

Used for:

* Reports for active/inactive users and time spent

.. _summary_usercoursesummary:
			
summary_usercoursesummary
---------------------------

Summary of users progress in a course

Columns:

* *id* - unique identifier for row in table
* *points* - number of points awarded for the user/course
* *total_downloads* - number of times the user has downloaded the course by downloading from the app when connecting to
  the server. Sideloaded courses will not count here, nor will courses who have been installed by other users
* *total_activity* - total number of activities attempted, for all versions of the course, so this number will equal
  total_activity_current + total_activity_previous
* *quizzes_passed* - unique number of quizzes passed, passing the same quiz twice or more will only count once. Only
  quizzes that are in the current version of the course will be counted.
* *badges_achieved* - number of badges a user has obtained for the course. Users can earn multiple badges if the pass
  the criteria for different versions of the course.
* *pretest_score* - percentage score in the pre-test, only applicable if the pre-test approach used is :ref:`content-quiz-pretest`
* *media_viewed* - unique number of media viewed, reaching the threshold to mark the media as completed. Watching the
  media twice (and reaching the completion threshold) will only count once. Only media in the current version of the
  course will be counted.
* *completed_activities* - total number of activities completed, each activity will only be counted once, and based on
  the current version of the course.
* *course_id* - id number of the course
* *user_id* - id number of the user
* *total_activity_current* - total number of activities attempted, for the current version of the course. If the same
  activity is in multiple versions of the course (including the current version), then it will be counted here.
* *total_activity_previous* - total number of activities attempted, for any previous version of the course. Only
  activities that are no longer in the current course version will be counted here.


Used for:

* Throughout the dashboard for graphs and showing users progress in courses
* Reports for course completion rates

.. _summary_userpointssummary:
		
summary_userpointssummary
--------------------------

Total points and badges achieved by user

Columns:

* *id* - unique identifier for row in table
* *points* - total number of points awarded to the user
* *badges* - total number of badges awarded to the user
* *user_id* - id number of the user

Used for:

* Leaderboards
