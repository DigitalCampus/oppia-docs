OppiaMobile Android App Change Log v7.x
=========================================


.. _appv91:

v91 (7.3.2) - not yet released
-------------------------------------------------------

 
Issue list:

* OPPIA-797 Gradle upgrade from 4.x to 7.x
* OPPIA-715 Add option to edit password and/or full profile
* OPPIA-822 Complete Indicator not working for quiz when threshold is 0
* OPPIA-763 Allow HTML layout in quiz/feedback questions and responses and quiz
  feedback

.. _appv90:

v90 (7.3.1) - Released 28 Sept 2021
-------------------------------------------------------

 
Issue list:

* OPPIA-733 Failing tests for androidTestFiles.UI.AdminProtectedUITest
* OPPIA-732 Failing test : androidTestFiles.FetchServerInfoTest > 
  fetchServerInfo_noConnection
* OPPIA-685 Tablet layout - Settings (on oppia-666-initial-tablet-layout
  branch)
* OPPIA-688 Tablet layout - Course index (on oppia-666-initial-tablet-layout
  branch)
* OPPIA-728 Check the changes to file storage access/permissions in Android 11
* OPPIA-756 Add option to retake quiz from Scorecard > Quizzes
* OPPIA-774 Improve theming for dark background colour
* OPPIA-777 Hide language change option if there is only one language
* OPPIA-726 Refactor to use android:paddingStart instead of paddingLeft etc
* OPPIA-786 Additional configuration option for video completion criteria 
  (GAMIFICATION_MEDIA_SHOULD_REACH_END)
* OPPIA-785 Allow page read time criteria to be configurable
  
  
.. _appv89:

v89 (7.3.0) - Released 15 Jul 2021 
-----------------------------------------------

.. note::
   There are changes in the theme and styling in this release, if you have a 
   custom theme for your app, then you should review it carefully after merging 
   this release in.
 
Issue list:

* OPPIA-725 Images and styles don't display in course content on Android 11
* OPPIA-676 Improve changing the theme colours/icon
* OPPIA-722 Retake quiz option not working
* OPPIA-723 Course quiz attempts screen not getting populated
* OPPIA-731 Add option to admin restrict changing server or accessing advanced
  settings

.. _appv88:

v88 (7.2.2) - released 22 Jun 2021
-----------------------------------------------

Issue list:


* OPPIA-647 Remove jCenter() from build.gradle (is deprecated)
* OPPIA-643 Implement course completion criteria in app
* OPPIA-592 Finalize refactorizing Payload objects
* OPPIA-651 Speed up retrieval of the leaderboard
* OPPIA-644 Set up course reminder notifications
* OPPIA-645 Allow users to set day/time of course reminder notifications

.. _appv87:

v87 (7.2.1) - released 24 May 2021
-----------------------------------------------

Issue list:

* OPPIA-604 NullPointerException on TagSelectActivity
* OPPIA-616 Improve "reset password" and "remember username" end flow
* OPPIA-626 Crash after login/logout if crash reporting is not enabled
* OPPIA-614 User ViewBinding instead of findViewById
* OPPIA-636 Check if online, for download data and delete account
* OPPIA-620 Add option for no bug tracking/analytics
* OPPIA-597 Fix issue with Ethiopian alphabet used in username (and other 
  non-latin scripts)
* OPPIA-612 Move analytics preferences to after registration and on per user 
  basis
* OPPIA-623 Option to download certificates from within the app
* OPPIA-657 Fix issue with tablet layout


.. _appv86:

v86 (7.2.0) - released 30 Apr 2021
-----------------------------------------------

.. note::
   For this version of the app, you will need to be running server v0.12.16 or
   above for the password reset, username reminder, account deletion and data
   download features to work correctly.
 
Issue list:

* OPPIA-584 Improved password reset process
* OPPIA-577 Create local app setting to determine when course updates were last
  checked
* OPPIA-578 Turn off nagging course update notifications
* OPPIA-603 Turn off couple of handled exception email reports
* Fix UserNotFound expection when user not logged in
* OPPIA-560 Add a privacy section to the app drawer menu
* OPPIA-561 Add opt in/out for the bug tracking and external analytics
* OPPIA-565 Allow users to delete their account from within the app
* OPPIA-579 Show notification when a new course is published
* OPPIA-580 Course deletion information
* OPPIA-581 Course update notification
* OPPIA-588 Create abstract class for bug reporting system
* OPPIA-585 Option to get reminder of username
* OPPIA-238 Quiz tests for matching questions
* OPPIA-593 Server change when logged in does not require admin pswd any more
* OPPIA-613 User APIkey after server change doesn't get invalidated
* OPPIA-562 Add option to download your data, from the app



.. _appv85:

v85 (7.1.9) - Released 1 Apr 2021
-----------------------------------------------

Issue list:

* OPPIA-548 On changing server setting, user is logged out
* OPPIA-141 Matching questions - text not wrapping
* OPPIA-549 Remove metadata that requires the read phone state permission
* OPPIA-90 TransactionTooLargeException when performing search with large result
  set
* OPPIA-570 Clicking on scorecard from home page may crash app
* OPPIA-107 Refactoring of AsyncTask 


.. _appv84:

v84 (7.1.8) - released 1 Mar 2021
-----------------------------------------------

Issue list:

* OPPIA-494 Clean AndroidStudio project structure view
* OPPIA-519 Points/gamification not disabled
* OPPIA-518 Cached login data not tied to the specific server
* OPPIA-506 Inform users of quiz pass threshold
* OPPIA-453 Allow feedback questions to be optional 
* OPPIA-526 Improve display of points in Points overview
* OPPIA-509 Logout text changed
* OPPIA-505 Display badge awarding criteria
* OPPIA-217 Add notification for course install failure on bluetooth transfer
* OPPIA-500 Quiz attempts for pre-tests are counted different in different
  places
* OPPIA-525 Quiz attempts discrepancy
* OPPIA-531 Spaces in media filename mean that the video cannot be downloaded
* OPPIA-554 Not saving email address
* OPPIA-530 Files resource naming can cause the app to fail to download a course


.. _appv83:

v83 (7.1.7) - Released 22 Dec 2020
-----------------------------------------------

Issue list:

* OPPIA-482 P2P transfer of larger courses doesn't complete
* OPPIA-483 Update SonarCloud to run on java 11
* OPPIA-498 Make + sign clickable
* OPPIA-499 Proper wording of activities in Points activity list
* OPPIA-464 Update gradle and libraries
* OPPIA-477 Better notifications when there had been errors downloading media
  files
* OPPIA-466 Solve storage location issues
* OPPIA-251 Quiz - add tests for baseline quizzes
* OPPIA-253 Quiz add tests for max no attempts
* OPPIA-501 Deleting courses doesn't delete media files


.. _appv82:

v82 (7.1.6) - Released 27 Nov 2020
-----------------------------------------------

Issue list:

* OPPIA-436 Add/create sql test data for testing the app with
* OPPIA-106 Refactor "widget" classes
* OPPIA-219 In FileUtils use try-with-resources
* OPPIA-463 OnUpButton pressed - go back to app homepage
* OPPIA-456 Add the stepped registration form to the core Oppia
* OPPIA-465 On the edit profile page, the email is required, even though the
  registration form defines it as optional
* OPPIA-452 On course index page show if there is missing media and option to
  download all

.. _appv81:

v81 (7.1.5) - Released 2 Nov 2020
-----------------------------------------------

Issue list:

* OPPIA-441 Remove option to download via PC
* OPPIA-257 DbListener redundant
* OPPIA-409 Error when doing release build
* OPPIA-421 Enable making password visible
* OPPIA-448 Drag and Drop quiz questions no longer work, so removed
* OPPIA-445 Update gradle libraries to most recent one
* OPPIA-416 Weblink/intent - allow using wildcards
* OPPIA-435 Add tests for CourseActivity class
* OPPIA-428 Possibility to login/register when opening the app via Intent/Link
* OPPIA-235 Complete BadgesUITest
* Additional automated tests

.. _appv80:

v80 (7.1.4) - Released - 30 Sept 2020
------------------------------------------------

Issue list:

* OPPIA-415 Version number checking fails when version name has alphanumeric 
  suffix
* OPPIA-387 Weblink/Intent for opening/downloading a specific course
* OPPIA-234 AboutUI tests
* OPPIA-393 Add tests for no courses installed notification


.. _appv79:

v79 (7.1.3) - Released 26 Aug 2020
------------------------------------

Issue list:

* OPPIA-322 Update the badges screen in the app
* OPPIA-323 Add a select and download all option to course downloading
* OPPIA-388 Allow the stepper registration form to be defined in the custom
  fields json

.. _appv78:

v78 (7.1.2) - released 31 July 2020
------------------------------------

Issue list:

* OPPIA-250 Fix code smells as result of updating min SDK version to 21 and
  other updates
* Bugfix for Android Intent
* OPPIA-350 Add app tests for the Feedback activity
* OPPIA-112 When quiz loading fails then give a proper error message
* OPPIA-348 Add tests for the new options of the custom fields

.. _appv77:

v77 (7.1.1) - released 1 July 2020
------------------------------------

Key updates:

* Improved options for custom registration fields
* Bug fixes
* Minimum Android supported is v5+

Issue list:

* OPPIA-282: Replace API endpoint with v2
* OPPIA-329: Use vector drawable for options menu icon
* OPPIA-330: Fix design of TagSelectActivity when empty
* OPPIA-332 Unable to install a course that has large embedded files
* OPPIA-290 Fix feedback activity
* OPPIA-345 Update Spanish translations
* OPPIA-184 Improve how custom registration form fields can be specified
* OPPIA-370 Min SDK set to 21
* OPPIA-354 On the custom fields, if a choices collection is changed, it 
  doesn't get updated in the app
* OPPIA-355 Only ask for the location access if a user tries to use the
  bluetooth option
* OPPIA-293 Save the time taken and the event type for feedback activities
* OPPIA-333 Issue with TTS not stopping when moving to another activity

.. _appv76:

v76 (7.1.0) - released 4 May 2020
------------------------------------

Key updates:

* Minimum Android supported is v6+ (Marshmallow)
* Improvements for colour/theme customisation

Issue list:

* OPPIA-248 Update the minSDKversion
* OPPIA-178 Initial fixes for feedback activity support
* OPPIA-311 TTS stops if screen is not flagged to stay on
* OPPIA-312 Update theming so more flexible to restyle
* OPPIA-299 Customising the app icon - use App.APP_LOGO
* OPPIA-327 Bluetooth menu icons don't appear on some branding - use vector 
  icons instead


.. _appv75:

v75 (7.0.5) - released 18 Mar 2020 
------------------------------------

Key updates:

* Revised settings screen layout
* SonarCloud coverage integration
* Increased test coverage, and many SonarCloud recommendations fixed
* Option to edit profile when online

Issue list:

* OPPIA-87 Rename layout "row" files for readability
* OPPIA-210 Decouple API endpoint in login screen
* OPPIA-213 Delete Admin remote control code
* OPPIA-211 Remove unused files and resources
* OPPIA-92 Github actions/workflows - add expected fail for tests that need
  internet connection
* OPPIA-208 Create test for installing course after backup course file has been
  created
* OPPIA-119 Initial Room migration for database
* OPPIA-123 Re-organise settings screen
* OPPIA-220 Change Register Toolbar size
* OPPIA-231 Fix vulnerability in HTTPClient Utils
* OPPIA-233 Rename ViewHolder classes that extend RecyclerView.ViewHolder
* OPPIA-109 SonarQube & Testing: Disable XML external entity (XXE) processing
* OPPIA-95 Add option for user to edit their profile - online only
* OPPIA-261 Replace deprecated PreferenceManager
* OPPIA-188 Saving time taken for each quiz attempt
* HOTFIX OPPIA-228 Errors when building normalRelease variant



.. _appv74:

v74 (7.0.4) - Released 4 Feb 2020 
------------------------------------

Key updates:

* Showing full detail of previous quiz attempts
* Improved Bluetooth sync interface

Issue list:

* 968: Update course scorecard to display quizzes as list
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/968
* 958: Default icon not showing with new interface
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/958
* 973: Several AdminProtection tests fail and hangs rest of test suite
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/973
* 969: From course scorecard, allow drilling down to specific quiz attempts
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/969
* 970: From global scorecard, show list of quizzes recently attempted, 
  plus full detail
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/970
* 982: App crashing when using back icon in course page
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/982
* 965: Fragment not attached error when checking endpoint in settings screen
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/965  
* 978: Bluetooth transfer - archive rather than delete activity logs that have
  been transferred
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/978
* 976: Bluetooth transfer - clarify the user messages
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/976  
* 975: Bluetooth transfer - combine the transfer and activity tabs
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/975 
* 979: Bluetooth transfer - larger icons for activity logs
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/979
* OPPIA-183 Better labels for activity logs on bluetooth transfer/sync screen

.. _appv73:

v73 (7.0.3) - Released 20 Dec 2019 
-----------------------------------

Key updates:

* Interface updates
* Additional tests
* Code refactoring

Issue list:

* 931: Check text colour on some interface elements
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/931
* 930: Add admin setting option to prevent changing of the server address
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/930
* 937: Scorecard activity graph - show "all activities" only by default
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/937  
* 948: Test `Services.TrackerWorkerTest` hangs
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/948
* 907: TrackerService generates error messages when no-one logged in
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/907 
* 950: On points list display make the scrolling for the whole page
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/950
* 856: Change (or remove) the publisher info on course download page
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/856
* 812: Replace ListView+ArrayAdapters with RecyclerView+RecyclerView.Adapters
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/812
* 936: Collapse all option on course index page
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/936
* 962: Fix all tests related with RecyclerView refactor
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/962
* 939: Test for ensuring question is answered before moving to the next
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/939
* 932: Add tests for the different options when admin password is set
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/932
 
.. _appv72:

v72 (7.0.2) - Released 28 Nov 2019 
-------------------------------------

Key updates:

* UI fixes/updates
* Review and updates for tracker data recording
* Additional automated tests

Issue list:

* 901: Course layout issue when switching between landscape and portrait
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/901
* 918: Tracker meta-data not always being recorded
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/918
* 919: Fix "Unselect all" button visibility
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/919
* 860: Review Google Messaging GCM
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/860 
* 917: Search tracker recording blank searches
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/917
* 886: ListPreference requires an entries array and an entryValues array
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/886
* 913: Offline registration - create tests to check it's not case sensitive
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/913
* 922: Quiz attempts being recorded multiple times in the tracker log
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/922
* 904: Update activity log export for media/quiz
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/904
* 895: Allow exported activity logs to be directly uploaded to the server
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/895
* 915: Tracker logs - confirm that completing page activities is working
  correctly
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/915
* 929: Test failure -  showsWelcomeActivityOnLogoutClickYes(
  UI.MainActivityUITest)
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/929
* 918: Tracker meta-data not always being recorded
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/918
* 940: Add specific test for implementation
  - https://github.com/DigitalCampus/oppia-mobile-android/issues/940

.. _appv71:

v71 (7.0.1) - beta version
--------------------------------------

Key updates:

* Updated user interface

Issue list:

* 880: Update the tests for the new UI - https://github.com/DigitalCampus/oppia-mobile-android/issues/880
* 779: SonarQube - fix input/output stream closure issues - https://github.com/DigitalCampus/oppia-mobile-android/issues/779
* 773: Check that all the current tests run properly - https://github.com/DigitalCampus/oppia-mobile-android/issues/773
* 889: Default view in Course List to expand and show all activities, with option to collapse - https://github.com/DigitalCampus/oppia-mobile-android/issues/889
* 896: Add new user preferences to save in DB - https://github.com/DigitalCampus/oppia-mobile-android/issues/896
* 890: Default course description = false in settings menu - https://github.com/DigitalCampus/oppia-mobile-android/issues/890
* 879: UI minor updates - after review - https://github.com/DigitalCampus/oppia-mobile-android/issues/879
* 893: Improve UI to make Bluetooth buttons more clear - https://github.com/DigitalCampus/oppia-mobile-android/issues/893
* 892: Bluetooth - Automatically export activities when you open the sync menu - https://github.com/DigitalCampus/oppia-mobile-android/issues/892
* 844: Add some test for new code and fix absolete ones (points animation, activities and points screen) - https://github.com/DigitalCampus/oppia-mobile-android/issues/844
* 908: Improve points views explanations in the docs - https://github.com/DigitalCampus/oppia-mobile-android/issues/i908

.. _appv70:

v70 (7.0.0) - alpha version only 
---------------------------------

Key updates:

* Updated user interface

Issue list:

* 866: Implement updated course activity page - https://github.com/DigitalCampus/oppia-mobile-android/issues/866
* 862: Implement redesigned home page - https://github.com/DigitalCampus/oppia-mobile-android/issues/862
* 867: Review and check the new theme on all screens - https://github.com/DigitalCampus/oppia-mobile-android/issues/867
* 864: Implement new drawer menu - https://github.com/DigitalCampus/oppia-mobile-android/issues/864
* 863: Implement bottom menu bar - https://github.com/DigitalCampus/oppia-mobile-android/issues/863
* 865: Implement new course index page - https://github.com/DigitalCampus/oppia-mobile-android/issues/865
* 885: Check gamification notifications working on new UI - https://github.com/DigitalCampus/oppia-mobile-android/issues/885
* 884: Bluetooth sync - make list of devices scrollable - https://github.com/DigitalCampus/oppia-mobile-android/issues/884
* 871: Tablet homepage design - https://github.com/DigitalCampus/oppia-mobile-android/issues/871

Previous Versions
------------------

.. toctree::
   :maxdepth: 2
   
   changelog_android_v6
   changelog_android_v5
   changelog_android_v4