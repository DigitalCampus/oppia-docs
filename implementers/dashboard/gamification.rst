Customising the Gamification (Points and Badges)
==================================================


.. note::
   * Updated points will not be applied on the users devices until they
     download the updated version of the course.
   * Changes to the course completion badge method will be applied straight away
   
The gamification events are defined as follows:

* `course_downloaded` - no points awarded for downloading the course
* `quiz_first_attempt` - no points for the first time the quiz is attempted
* `quiz_attempt` - no points each subsequent attempt at a quiz (max. once per 
  day per quiz)
* `quiz_first_attempt_threshold` - the quiz score percentage needed to get the 
  `quiz_first_attempt_bonus`
* `quiz_first_attempt_bonus` - bonus points for getting at least the 
  `quiz_first_attempt_threshold` in the quiz on the first attempt
* `activity_completed` - no points for the completing a page activity (max. once per day per activity)
* `media_started` - no points for starting to play a media file (max. once per day per media)
* `media_playing_interval` - number of seconds the media needs to be played to get the `media_playing_points_per_interval`
* `media_playing_points_per_interval` - no points for each `media_playing_interval`
* `media_max_points` - maximum number of points available for each media view

.. _change_default_points:

Changing the Global/Default Points
------------------------------------

You can edit the global/default points by:

#. Go to the Django Admin pages
#. Go to `Gamification` > `Default Gamification Events`
#. Select the event to change the points for and save

.. _customise_points:

Customising Course and Activity Level Points
----------------------------------------------

To customise the points for a particular course and its activities:

#. Go to the courses list in the Oppia server dashboard
#. Click on the `Gamification Settings` icon for the course to update (the icon 
   on the far right of the row)
   
   .. image:: images/gamification1.png
   
#. You'll now see the gamification customisation screen:

   .. image:: images/gamification2.png
   
#. If you'd like to change the points at the course level (e.g. so every quiz in
   the course has 50 points for the first attempt, rather than the default of 
   20), then select the `Course global settings`, then `Edit settings`:
   
   .. image:: images/gamification3.png
   
#. If you'd like to change the points just for a specfic activity, perhaps the
   final quiz gives users more points than other quizzes, expand the relevant
   topic in the course structure and navigate to the activity you'd like to
   update, then click the edit icon:
   
   .. image:: images/gamification4.png
   
#. For updating the points for the media that are included in the course, these
   are listed at the end of the course structure, under the `Media elements`
   section:

   .. image:: images/gamification5.png

   
.. note::
   Remember to click the save settings button at the end of the page after you 
   are finished with editing the points.
   
Change course complete badge award method
-------------------------------------------

#. Go to the Django Admin pages
#. Go to `Oppia` > `Badges`
#. Click on the ``Course completed`` record to edit it
#. Change the ``default  method`` field to the method you'd like to use, then
   save
   
Change percentage of activities needed to complete the course
--------------------------------------------------------------

.. note::
   This setting is only used when the course complete badge award method is set
   to `all_quizzes_plus_percent`

#. Go to the Django Admin pages
#. Go to `Settings` > `Settings`
#. Click on the ``OPPIA_BADGES_PERCENT_COMPLETED`` record to edit it
#. Change the ``int value`` field to the percentage you'd like to use, then
   save
   