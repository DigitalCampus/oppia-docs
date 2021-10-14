OppiaMobile Moodle Block Change Log
=====================================



.. _blockv1.2.10:

v1.2.10 - not yet released
------------------------------------

* OPPIA-758 Too aggressive replacement of video file content



.. _blockv1.2.9:

v1.2.9 - Released 24 Sept 2021, updated 5 Oct 2021
-------------------------------------------------------

* OPPIA-769 Error in block when debug output is enabled
* OPPIA-805 Error on upgrading block

.. _blockv1.2.8:

v1.2.8 - Released 16 July 2021
------------------------------------

* OPPIA-671 Export block tag/categories can get extra '-' added
* OPPIA-727 Update version of jquery used in block

 
.. _blockv1.2.7:

v1.2.7 - Released 1 July 2021
------------------------------------

* OPPIA-154 Remove code related to export2print
* OPPIA-713 New course style for Extension Essential app
* OPPIA-670 Review SonarCloud Lint issues

.. _blockv1.2.6:

v1.2.6 - Released 20 May 2021
------------------------------------

* OPPIA-594 Shouldn't be able to progress to final export step if videos not
  exported yet

.. _blockv1.2.5:

v1.2.5 - Released 29 Apr 2021
------------------------------------

* OPPIA-552 Page with video export doesn't pick up the video poster image

.. _blockv1.2.4:

v1.2.4 - Released 26 Mar 2021
------------------------------------

* OPPIA-453 Allow feedback questions to be optional
* OPPIA-538 How to handle courses with multiple (identical) activities that have
  same digest
* OPPIA-150 Remove check to see the server/block version for the type of quiz
  export
* OPPIA-550 Feedback activities get exported as new activities on every export
* OPPIA-551 Solved issue that only loaded the first embedded video in a page
  activity
* OPPIA-530 Replace filesystem and URI unsafe characters for resource files

.. _blockv1.2.3:

v1.2.3 - Released 23 Dec 2020
------------------------------------

* OPPIA-162 Allow deleting of server connections
* Allow quiz pass threshold to be set to 0%
* HOTFIX (2 Feb 2021) for video embedding

.. _blockv1.2.2:

v1.2.2 - Released 27 Nov 2020
------------------------------------

.. warning::
	Version 1.2.x and above of the block requires you to be using Oppia server
	version 0.12.12 or above

* OPPIA-437 New export block not including media length
* OPPIA-442 Not picking up course status for title display
* OPPIA-443 Video embed file doesn't pick up a new version

.. _blockv1.2.1:

v1.2.1 - beta version only
------------------------------------

* OPPIA-434 Change the content that the md5 digest is based on


.. _blockv1.2.0:

v1.2.0 - alpha version only
------------------------------------

* OPPIA-286 Initial development for extracting Moodle embedded media from page
  activities
* OPPIA-417 Retain the default server connection, even after a user adds their
  own
* OPPIA-446 Begin to set up unittests for the Moodle Oppia export block
* OPPIA-448 Drag and Drop quiz questions no longer work, so removed


.. _blockv1.1.3:


v1.1.3 - Released 25 Oct 2020
------------------------------------

.. warning::
	Important Note: This release changes the digests for all activities, so any
	courses published with this version of the block, will have the activities
	set as new. This is a one-off change for future proofing if the Moodle
	activity object definition changes.

* OPPIA-434 Change the content that the md5 digest is based on


.. _blockv1.1.2:

v1.1.2 - Released 20 Oct 2020
------------------------------------

* OPPIA-459 Course and activity icon fixes


.. _blockv1.1.1:

v1.1.1 - Released 29 Sept 2020
------------------------------------

* OPPIA-384 Server connections in Moodle export block - API key no longer
  necessary
* OPPIA-383 Improve how draft courses are handled

.. _blockv2020082400:

v2020082400 - Released 24 Aug 2020
-------------------------------------

* OPPIA-320 Image export can fail if image has been overwritten in Moodle


.. _blockv2020072800:

v2020072800 - Released 28 July 2020
-------------------------------------

* OPPIA-366 On export from Moodle hidden activities are still being exported


.. _blockv2020051600:

v2020051600 - Released 16 May 2020
-------------------------------------

* OPPIA-290 Finalise option to support Feedback activities
* OPPIA-377 Update other moodle/oppia css styles for the other 2 options


.. _blockv2020040401:

v2020040401 - Released 4 Apr 2020
-------------------------------------

* OPPIA-178 Fix issue with exporting feedback activities
* Remove redundant code for processing/submitting quizzes directly to the
  server
* OPPIA-321 Stylesheet for nested lists

.. _blockv2020020101:

v2020020101 - Released 1 Feb 2020
-------------------------------------

* OPPIA-201 Fix issue with deleted activities still getting exported 
* OPPIA-147 Remove quiz 'availability' option
* OPPIA-148 Remove quiz 'allow try-again' option
* OPPIA-149 Rename 'tags' to be 'categories' to match app and server
* OPPIA-159 Rename 'stylesheet' to 'course design profile' or similar

.. _blockv2019103100:

v2019103100 - Released 31 Oct 2019
-------------------------------------

* 205: Downloading course file directly should be much less prominent - 
  https://github.com/DigitalCampus/moodle-block_oppia_mobile_export/issues/205

.. _blockv2019102800:

v2019102800 - Released 28 Oct 2019
-------------------------------------

* 192: In Moodle version 3.5+ (Build: 20180531), the DB installation XML causes 
  an error with the PATH attribute - 
  https://github.com/DigitalCampus/moodle-block_oppia_mobile_export/issues/192
* 204: Add logging for course publishing - 
  https://github.com/DigitalCampus/moodle-block_oppia_mobile_export/issues/204

Previous Versions
------------------

.. toctree::
   :maxdepth: 2

   changelog_block_2018