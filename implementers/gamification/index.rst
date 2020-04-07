Points and Badges
====================

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

Changing the Global/Default Points
------------------------------------

You can edit the global/default points by:

#. Go to the Django Admin pages
#. Go to the `Gamification` > `Default Gamification Events`
#. Select the event to change the points for and save


Customising Course and Activity Level Points
----------------------------------------------

To customise the points for a particular course and its activities:

#. Go to the courses list in the Oppia server dashboard
#. Click on the `gamification` icon for the course to update (the icon on the
   far right of the row)
#. Edit the course level points and/or the points for a specific activity, then
   press save
   
.. note::
   The updated points will not be applied on the users devices until they
   download the updated version of the course onto their device.

Badges and Completing Courses
------------------------------

Every activity has the concept of 'completedness' and to be awarded a badge the
user must complete every activity in the course. The definitions of activities
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

To change the criteria for assessing completedness of the activities, the
getActivityCompleted() function for the relevant activity widget class in the
app code will need to be updated.


.. note::
   The badge awarding is performed by the :ref:`Oppia cron task <installcron>`,
   so for badges to be awarded, please ensure that the cron task is set up to 
   run regularly.

.. note::
    The Points shown in the bottom bar are the total points users have earned 
    (even if they have logged in on many devices). This points view might not
    match with the total points shown in the Points section which shows the
    list of activities and points on the local device. 

