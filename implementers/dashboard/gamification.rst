Customising the Gamification (Points and Badges)
==================================================


.. note::
   * Updated points will not be applied on the users devices until they
     download the updated version of the course.
   * Changes to the course completion badge method will be applied straight away
   

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
#. Click on the `gamification` icon for the course to update (the icon on the
   far right of the row)
#. Edit the course level points and/or the points for a specific activity, then
   press save
   
   
Change course complete badge award method
-------------------------------------------

#. Go to the Django Admin pages
#. Go to `Oppia` > `Badges`
#. Click on the ``Course completed`` record to edit it
#. Change the ``default  method`` field to the method you'd like to use, then
   save
   
Change course complete badge award method
-------------------------------------------

#. Go to the Django Admin pages
#. Go to `Settings` > `Settings`
#. Click on the ``OPPIA_BADGES_PERCENT_COMPLETED`` record to edit it
#. Change the ``int value`` field to the percentage you'd like to use, then
   save
   