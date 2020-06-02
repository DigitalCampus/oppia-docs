Database table descriptions
==============================

The tables are shown below in alphabetical order:


auth_user
----------

Stores the basic user information, such as username, password, email, name etc.
This is a core Django framework table.

oppia_activity
-----------------

Stores the detail of the activities (pages/quizzes etc) associated with each
section in a course.

oppia_award
--------------

Stores the detail of the badges that have been awarded to users, for the
courses they have completed.

oppia_awardcourse
-------------------

Links the badges awarded to a user to a specific version of the course.

oppia_badge
----------------

Stores the detail of the badges that available to users.

oppia_course
--------------

Stores the detail of the courses available.

oppia_points
---------------

Stores the points that have been given to users for their engagement in
activities.

oppia_section
---------------

Stores the detail of the sections of activities within a specific course.

oppia_tracker
-----------------

Stores the detail of the activities and actions of a user.

profile_customfield
----------------------

Defines the specific fields that are displayed on the registration form.

profile_userprofile
----------------------

Additional registration form fields that are not included in the `auth_user`
table, but will be common almost all implementations.

profile_userprofilecustomfield
------------------------------------

Stores the detail of the user registration form responses for the 
`profile_customfield` entries.

quiz_quizattempt
------------------

Stores the detail of the quizzes (and feedback) a user has completed.

quiz_quizattemptresponse
---------------------------

Stores the detail of the individual quiz and feedback responses a user has 
given for each quiz and feedback question.

quiz_question
----------------

Stores the individual quiz questions.

quiz_quiz
-----------

Stores the quizzes and feedback that are in the courses.

quiz_quizquestion
--------------------

Links the quiz/feedback to the specific questions.

quiz_response
---------------

Stores the responses available for each quiz question.