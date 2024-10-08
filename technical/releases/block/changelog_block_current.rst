OppiaMobile Moodle Block Change Log
=====================================


.. _blockv1.4.11:

v1.4.11 - not yet released
------------------------------------------------


Issue list:


.. _blockv1.4.10:

v1.4.10 - released 28 Aug 2024
------------------------------------------------


Issue list:

* OPPIA-1625 Fix issue with quiz digests show as to preserve
* OPPIA-1641 Fix issue with multiple langs not getting exported
* OPPIA-1647 Allow multiple audio files in single activity



.. _blockv1.4.9:

v1.4.9 - released 10 Apr 2024
------------------------------------------------

.. note::

    **Backwards compatibility issue**: The functionality to be able to show
    questions feedback only after the question is answered is not compatible
    with Android app v7.4.6 and previous. In previous versions, if a quiz is
    configured to only show feedback after each question is answered, it will
    behave as if it was configured to never show feedback.

Issue list:

* Add NooraHealth style package
* OPPIA-1627 Add option to only to display feedback after each question


.. _blockv1.4.8:

v1.4.8 - released 29 Feb 2024
------------------------------------------------



.. note::

    Archived themes have been moved to the /styles/archive/ folder

Issue list:

* OPPIA-1552 Record server version when publishing
* OPPIA-1613 Fix issue with saving pre-test configurations
* OPPIA-1620 Archive themes no longer supported by Digital Campus
* OPPIA-1559 Show standard instructions on multichoice and multiselect questions
* OPPIA-1621 Export quiz questions, responses and feedback as HTML files


.. _blockv1.4.7:

v1.4.7 - released 13 Dec 2023
------------------------------------------------

Requires Moodle 4.1 LTS and PHP v8

Issue list:

* OPPIA-1404 Update for Moodle 4.1 LTS
* OPPIA-1608 Fix quiz question image exporting

.. _blockv1.4.6:

v1.4.6 - released 5 Oct 2023
------------------------------------------------

Issue list:

# OPPIA-1578 Conflict with function name: resize_image

.. _blockv1.4.5:

v1.4.5 - released 29 Jun 2023
------------------------------------------------

.. note::
    When the Moodle upgrade completes, run the following command:

    *php migrations/v1.4.5_migrations.php*

    This will remove duplicate server URLs. Verify that there are no
    duplicate URLs in the Oppia Export Block server's dropdown.

Issue list:

* OPPIA-1556 Remove and prevent duplicated server urls


.. _blockv1.4.4:

v1.4.4 - released 31 May 2023
------------------------------------------------

Issue list:

* OPPIA-1430 Fix unused variable issues raised in PHP Mess Detector report
* OPPIA-1429 Fix Moodle Code Checker errors and warnings
* OPPIA-1500 Export embedded PDFs in page activities as course resources
* OPPIA-1517 Check in export process if activity is of unsupported type
* OPPIA-1534 Error Publishing Course - xml validation failing
* OPPIA-1542 Fix extract_langs function call in tests


.. _blockv1.4.3:

v1.4.3 - released 31 Mar 2023
------------------------------------------------

Issue list:

* OPPIA-1396: Update CI build workflow.
* OPPIA-1426: Updated message when no feedback activities with rated questions exist
* OPPIA-1454: Don't ignore server id on grade boundaries db request
* OPPIA-1330 Review and update block code style

.. _blockv1.4.2:

v1.4.2 - released 28 Feb 2023
------------------------------------------------

Issue list:

* OPPIA-1346: Add multi-lingual support for grade boundaries
* OPPIA-1366: Pass activity digests from previous step so we don't have to process the course again
* OPPIA-1304: Remove some PHP warnings in code
* OPPIA-1363: Clean saved password if the field is emptied
* Hotfix: Increase message field length and limit textarea


.. _blockv1.4.1:

v1.4.1 - released 31 Jan 2023
------------------------------------------------

.. note::
    * Moodle currently only supports PHP 8.0 (not PHP 8.1)
    
Issue list:

* OPPIA-1361 Update for PHP v8
* OPPIA-1359 Fix missing description field
* OPPIA-1360 Update Moodle question id properties considering Moodle 4 Question Bank update
* OPPIA-847 Error when uploading and media file is included twice in the same course
* OPPIA-1365 Add moodle_question_id to feedback activities on export
* OPPIA-1303 Additional automated tests for Moodle Block


.. _blockv1.4.0:

v1.4.0 - released 30 Nov 2022
------------------------------------------------

.. note::
	* Moodle 4 is required.
	* You may need to update the multilang filter in Moodle after upgrading, see 
	  https://docs.moodle.org/en/Multi-language_content_filter, check that the multilang filter is enabled, and set to
	  be applied to "content and headings".

Issue list:

* OPPIA-1306 Upgrade for Moodle 4
* OPPIA-837 Refactor for multi-lang titles during export
* OPPIA-764 Automatically add a 'play' button overlay to video images
* OPPIA-1289 Cumulative Display for Feedback Activity
* OPPIA-1342 On Export step 4 use a POST request
* OPPIA-1344 Course XML not found message on Step 5 of moodle export

.. _blockv1.3.6:

v1.3.6 - released 31 Oct 2022
------------------------------------------------

Upgrade notes
^^^^^^^^^^^^^
A management script was added to be able to import previously published courses from the block and
update the digests table based on its contents. This would allow to retain the actual identifiers that
are currently published in the Oppia server, instead of the digest from the current version of each activity.

For this, you need to download from the OppiaMobile server the courses you want to import the digests from,
and obtain the course's ``module.xml`` file. Then, you will need to run the script:

```
php ./scripts/import_course_digests.php path/to/module.xml
``` 
(from the oppia_mobile_export directory, on the command line)

This script will traverse the course XML and try to match the activities to the current ones in Moodle. For
quiz activities, if the course was exported after the `v1.3.0` release, the Moodle quiz ID will be use to
obtain the activity. In the rest of the cases, it will try to match against the activity title.
It will give a comprehensive report for all the activities, indicating the digest saved, and the previously
preserved digest (if any).

**Note**: If the course was exported in "draft" mode, a `-draft` suffix is added to its shortname. This is taking
into account in the script if the course is not found with its complete shortname in Moodle. 


Issue list:

* OPPIA-1278 Retain last selected course design
* OPPIA-55 On publishing & max upload size is exceeded - unclear error message
* OPPIA-1268 Management script for importing existing published course and updating MD5 table
* Fix issue with section titles and Moodle internal multilang filter
* OPPIA-1281 Lock feedback activity with password
* OPPIA-1293 Republishing without any changes always flags with option to preserve identifier
* OPPIA-1270 Initial setup for automated tests
* OPPIA-1296 Update text on course publishing report page


.. _blockv1.3.5:

v1.3.5 - released 30 Sept 2022, updated 18 Oct 2022
-------------------------------------------------------

Upgrade notes
^^^^^^^^^^^^^
For the option to preserve identifiers (OPPIA-1265), you will need to run the script:

``php ./migrations/20220929_migrate_script.php`` (from the oppia_mobile_export directory, on the command line)

The script currently outputs raw HTML, but you don't need to do anything with this HTML, but if you want to save/review
you can pipe the output to a file, eg ``php ./migrations/20220929_migrate_script.php > /path/to/file/output.html``

This prefills the data with the current course activity versions, so on the next course publishing you will get the
option to preserve the identifiers for the activities you have changed. You only need to run this script once, running
the script again will reset the activity identfier logs. 

If the script is not run, the only difference is that the first time you publish the course after updating the block to
this version, you won't get any option to preserve any identifiers, only subsequent time you update and publish the
course.

For restricting feedback activities to single response (OPPIA-762), if you want to allow multiple submissions, then you
will need to edit the feedback settings, as the default in Moodle is to restrict to single response.

Issue list:

* OPPIA-1274 Change location of output folder
* OPPIA-1277 Allow use of non-latin script in course shortname
* OPPIA-1287 Fix regex in multichoice (rated) questions
* OPPIA-762 In feedback activity allow just a single attempt
* OPPIA-1315 Issue with exporting HTML files
* OPPIA-1265 Option to preserve activity identifiers:

   * OPPIA-1266 Create new table for storing current activity MD5s
   * OPPIA-1267 Create script for baseline MD5s
   * OPPIA-1272 New export step to allow selection of preserving ids/MD5
   * OPPIA-1273 Update MD5s in block table (only on publishing to Oppia server)
   * OPPIA-1294 Changing quiz title then recreates the questions in Oppia
   * OPPIA-1292 Change in quiz title doesn't give option to preserve identifier
   * OPPIA-1294 Change text for "no changes detected"

.. _blockv1.3.4:

v1.3.4 - released 28 June 2022
------------------------------------

* OPPIA-832 Additional inline question type - for authors to require an input field before feedback/answer is revealed

.. _blockv1.3.3:

v1.3.3 - released 30 May 2022
------------------------------------

* OPPIA-1202 Fix issue with multi-lang section titles
* OPPIA-1208 Decode utf-8 chars before parsing with libxml to avoid encoding
  issues

.. _blockv1.3.2:

v1.3.2 - released 26 Apr 2022
------------------------------------

* OPPIA-1087 In JSON object, feedback activity description is filled with
  "pre-test"
* OPPIA-1184 Ignore page breaks in Moodle feedback activities

.. _blockv1.3.1:

v1.3.1 - released 28 Mar 2022
------------------------------------

* OPPIA-865/1012 Add skip logic for feedback activities
* OPPIA-1004 Update for Moodle 4 compatibility

.. _blockv1.3.0:

v1.3.0 - released 28 Feb 2022 (updated 8 Mar 2022)
---------------------------------------------------

* OPPIA-938/1009 Allow adding of password to lock a topic
* OPPIA-938/955 Update the XSD to validate the generated module.xml file
* OPPIA-880 Include Moodle quiz and question id nos when exporting data
* OPPIA-1085 Fix quiz feedback setting

.. _blockv1.2.13:

v1.2.13 - released 30 Jan 2022
------------------------------------

* OPPIA-900 and OPPIA-945 Add option to prevent display of right/wrong answers 
  at end of quiz 
* OPPIA-833 Split out styles/javascript between core/custom for course styles


.. _blockv1.2.12:

v1.2.12 - released 29 Dec 2021
------------------------------------

* OPPIA-902 and OPPIA-933 Restrict access to quizzes with password
* OPPIA-927 Course sequencing setting not retained on re-export


.. _blockv1.2.11:

v1.2.11 - Released 14 Nov 2021
------------------------------------

* OPPIA-891 Fix for maxattempts not being saved correctly

.. _blockv1.2.10:

v1.2.10 - Released 29 Oct 2021
------------------------------------

* OPPIA-758 Too aggressive replacement of video file content
* OPPIA-794 Fix issue with non-ascii characters in image filenames
* OPPIA-763 Allow HTML layout in quiz/feedback questions and responses and quiz
  feedback
* OPPIA-783 Allow adding topic icons/images


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


Previous Versions
------------------

.. toctree::
   :maxdepth: 1

   changelog_block_2020
   changelog_block_2019
   changelog_block_2018
