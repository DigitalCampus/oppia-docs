Gamification - Points and Badges
==================================

OppiaMobile awards points and badges to users based on their usage of the app and content.

The points system is essentially a measure of engagement with the content - however it doesn't 
really give a picture of how much was understood. The badging provides confirmation that all 
the activities have been completed and that the user has met at least the pass threshold for 
each quiz included in the course.

Points System
-----------------

Points can be customised down to individual activity level, there are 3 levels 
of points:

* Activity Level Points - points which are defined for a particular activity.
* Course Level Points - points which are defined for a particular course. Each
  activity will use these points, unless an activity has had custom points set
  up.
* Global/Default Level Points - if neither course nor activity level points 
  have been defined, then the global/default points will be used.
  

Global/Default Points
-----------------------

By default, points are awarded as follows:

* 100 – creating an account
* 50 – downloading a course
* 20 – first time a quiz is attempted
* ? – depends on percentage score for a first attempt at a quiz. E.g. if the score is 75% on the 
  first attempt, 75 points will be awarded
* 50 – bonus for getting 100% on first attempt at a quiz
* 10 – each subsequent attempt at a quiz (max. once per day per quiz)
* 10 – completing an activity (max. once per day per activity)
* ? – video views – points are awarded for how long the video has been have watched, 5 points for 
  every 30 seconds watch, up to a maximum of 200 points. A bonus 20 points are given for the first 
  time in a day a particular video is watched

The points system is designed to encourage users to return to the courses regularly and engage in 
the activities.

To update the points see :doc:`../dashboard/gamification`
   

Badges and Completing Courses
------------------------------

Every activity has the concept of 'completedness'. The definitions of activities
being completed of each activity type are given below:

* quiz - a quiz is completed if the user has obtained at least the pass
  threshold for the quiz.
* text/webpage - the page must be open for at least 3 seconds. Clearly this is
  not a very effective measure of testing whether the user has fully read and
  understood the page content, however, currently it is the only way of
  measuring that we currently have. We advise ensuring that the quiz questions
  provide an effective measure of understanding the content.
* video - video/media files are embedded within text/web pages. The user must
  have the video running for at least the length of the video. This may not
  correspond exactly to saying they have watched the whole video - for example
  they may pause, fast-forward/rewind, and so have the video open for the
  required time, but not actually have watched the video from start to finish.
* feedback - the user needs to answer all the questions
* file - the user simply needs to have opened the file


Course completed badge options
---------------------------------

There are 4 options for the method to award a course completed badge:

* ``all_activities`` (default) - All activities must be completed, including 
  all quizzes passed and all media viewed
* ``all_quizzes`` - All quizzes need to be completed and passed
* ``final_quiz`` - Only the final quiz needs to be completed and passed
* ``all_activities_plus_percent`` - All quizzes need to be completed and passed,
  and a percentage (default is 80%) of all other activities completed. 
  This percentage is configurable in the settings.


To update the badge award method, or to change the percentage for the 
``all_activities_plus_percent`` method see :doc:`../dashboard/gamification`

.. note::
   The badge awarding is performed by the :ref:`Oppia cron task <installcron>`,
   so for badges to be awarded, please ensure that the cron task is set up to 
   run regularly. 

