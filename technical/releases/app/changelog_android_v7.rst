OppiaMobile Android App Change Log v7.x
=========================================


.. _appv115:

v114 (7.4.10) - not yet released
------------------------------------------------------

Issue list:


.. _appv114:

v114 (7.4.9) - released 30 Aug 2024
------------------------------------------------------

Issue list:

* OPPIA-1610 Update gradle and libraries
* OPPIA-1666 Update to explicitly confirm privacy policy
* OPPIA-1647 Allow multiple audio files in single activity
* OPPIA-1643 Additional fixes for points consistency




.. _appv113:

v113 (7.4.8) - released 22 Jul 2024
------------------------------------------------------

Issue list:

* OPPIA-1653 Update for Android 14 (API 34)
* OPPIA-1633 Update audio player for mp3 files
* OPPIA-1643 Fix for points consistency

.. _appv112:

v112 (7.4.7) - released 11 Apr 2024
------------------------------------------------------

Issue list:

* OPPIA-1611 Fix lint warnings on drawer_header
* OPPIA-1612 Update current funder information
* OPPIA-1621 Allow images and rich HTML in quiz question feedback
* OPPIA-1559 Show standard instructions on multichoice and multiselect questions

.. _appv111:

v111 (7.4.6) - released 30 Jun 2023
------------------------------------------------------

Issue list:

* OPPIA-1463 Update target Android API level to 33
* OPPIA-1509 Add external resource opening as completion criteria for page activities
* OPPIA-1561 Allow Unauthenticated Usage of "Offline Import Courses" Feature
* OPPIA-1565 SD card Error - Oppia Mobile Appication failing to open after instalation
* OPPIA-1566 Finish all the activitites in the backstack and display the login screen on back button pressed
* OPPIA-1568 Modified update activity task. now it is launched on each online login
* OPPIA-1569 "Offline course install" feature: Update unzip logic and update permission handling


.. _appv110:

v110 (7.4.5) - released 31 May 2023
-------------------------------------------------------

Issue list:

* OPPIA-961 App crashes if SD card is removed
* OPPIA-1483 Automated course and multimedia side-loading
* OPPIA-1494 'Retake the Quiz' button should be visible at the end of every Quiz with Unlimited attempts
* OPPIA-1542 Fix extract_langs function call in tests
* OPPIA-684/OPPIA-1503 Open and display the pdf contents when clicked.
* OPPIA-1536 Unable to open PDF File in Oppia in newer versions of Android

.. _appv109:

v109 (7.4.4) - released 27 Apr 2023
-------------------------------------------------------

Issue list:

* OPPIA-1482 Checking media file data exists.
* OPPIA-1427 Send analysis to sonarcloud
* OPPIA-969: Update user profile in app when it has been changed on the server
* OPPIA-1053, OPPIA-1484 Add tests for AsyncTasks
* OPPIA-1053, OPPIA-1485 Add tests for Activities
* OPPIA-1053, OPPIA-1486 Added tests to fragments and util classes
* OPPIA-395 More tests quiz activity


.. _appv108:

v108 (7.4.3) - released 31 Mar 2023
-------------------------------------------------------

Issue list:

* OPPIA-1439 Take course into account when fetching quiz and feedback attempts
* OPPIA-1311 Moved quiz model tests to unit tests

.. _appv107:

v107 (7.4.2) - released 28 Feb 2023
-------------------------------------------------------

Issue list:

* OPPIA-1410 Round off performance score values and add tests
* oppia-1364 Added notification permission
* Oppia 1324 apikey invalidate
* oppia-1310 BuildConfig settings in App class removed
* OPPIA-1346 Add multi-lingual support for grade boundaries


.. _appv106:

v106 (7.4.1) - released 31 Jan 2023
-------------------------------------------------------

Issue list:

* OPPIA-1348 Add tests for grade boundaries functionallity
* OPPIA-1349 Integrate Gradle Managed Devices 
* OPPIA-1323 Clearer messages when offline and password incorrect
* OPPIA-1054 Follow up to running app tests

.. _appv105:

v105 (7.4.0) - released 30 Nov 2022
-------------------------------------------------------

Issue list:

* OPPIA-764 Provide in-app option to select interface language
* OPPIA-1318 Invalidate activity icon image cache on course install
* OPPIA-1339 Fix for feedback password protection when there is a label as the first item in the feedback
* OPPIA-1305 Update gradle and other library updates
* OPPIA-1289 Cumulative Display for Feedback Activity


.. _appv104:

v104 (7.3.14) - released 31 Oct 2022
-------------------------------------------------------

.. note::
	If you are using Splunk Mint for the opt-in analytics, you must now move to Count.ly (or no opt-in analytics),
	Splunk Mint is no longer active, and no crash/analytics will be recorded by their systems anyway.

Issue list:

* OPPIA-1309 Remove Splunk Mint library option for analytics (Project entered End of Life)
* OPPIA-1090 Remove or replace usage of e.printStackTrace
* OPPIA-1281 Lock feedback activity with password
* OPPIA-1127 Reorganise test file structure
* OPPIA-1104 Option to auto-download user course activity on login, when connection is available
* OPPIA-1225 Fix unsafe zipping pattern


.. _appv103:

v103 (7.3.13) - released 30 Sept 2022
-------------------------------------------------------

Issue list:

* OPPIA-1093 Update Gradle and remove deprecation warnings for Gradle 8
* OPPIA-762 In feedback activity allow just a single attempt
* OPPIA-1256 Better error message if disk is full when installing course

.. _appv102:

v102 (7.3.12) - Fix release 10 Sept 2022
-------------------------------------------------------

Issue list:

* OPPIA-1280 Error logging in / downloading courses  - cohorts field not
  returned from older server versions

v102 (7.3.12) - released 31 Aug 2022
-------------------------------------------------------

Issue list:

* OPPIA-1217 Update OPPIA_SERVER_DOMAIN property in oppia-default.properties file
* OPPIA-1263 Change flush course cache to be flush app cache
* OPPIA-1193 Update for theme colour consistency

.. _appv101:

v101 (7.3.11) - released 27 Jul 2022
-------------------------------------------------------

Issue list:

* OPPIA-1259 Fix crash in tablet layouts with the new status badge
* OPPIA-1121 Enhance cohort capability to make a specific course accessible to only certain user group


.. _appv100:

v100 (7.3.10) - released 28 Jun 2022
-------------------------------------------------------

Issue list:

* OPPIA-1214 Update gradle to 7.2.0 and check for other library updates
* OPPIA-1134 Add Java 8 api compatibility
* OPPIA-1196 Remove logging of some UserNotFoundExceptions to analytics logs
* OPPIA-832 Save response from inline input
* OPPIA-1243 Issue with videos not playing
* OPPIA-1244 Fix for draft course not appearing in app
* OPPIA-1223 Course category shows in the count badge only the number of live courses
* Add API matrix for Github actions
* OPPIA-1195 Update feedback skip logic

.. _appv99:

v99 (7.3.9) - released 1 Jun 2022
-------------------------------------------------------

Issue list:

* OPPIA-1165 Simplify how course status is represented
* OPPIA-1173 Add icons in app for the course status
* OPPIA-1202 Fix issue with multi-lang section titles
* OPPIA-1209 Same language listed twice
* OPPIA-1206 Changing language in specific activity takes users back to first
  activity in the topic
* OPPIA-1212 Download tracker duplicated
* OPPIA-1166 Media missing event being tracked incorrectly
* OPPIA-1206 Changing language in specific activity takes users back to first activity in the topic
* OPPIA-1210 Retain position in quiz/feedback when changing language halfway through


.. _appv98:

v98 (7.3.8) - Released 3 May 2022
-------------------------------------------------------

Issue list:

* OPPIA-1143 Update DbHelper method unlockedsectionsCount
* OPPIA-1084 Show Feedback progress text in not required questions
* OPPIA-988 Add helper text on Username / Password registration fields
* OPPIA-1089 Replace Random with SecureRandom
* OPPIA-995 The compulsory field asterix is sometimes red, sometimes green
  (should always be red)
* OPPIA-1072 Update for new course status (new_download_only)
* OPPIA-1189 Lock topics password height cut off / text update
* OPPIA-1192 Fix for skip logic branching


.. _appv97:

v97 (7.3.7) - Released 31 Mar 2022
-------------------------------------------------------

Issue list:

* OPPIA-1031 Update Gradle and build libraries
* OPPIA-865 Add skip logic for feedback activities
* OPPIA-1045 Remove commented code
* OPPIA-1042 Replace string literals
* OPPIA-952 Add message on app homepage if connected to staging server
* OPPIA-1044 Thread.sleep should not be used, replaced with awaitility library
* OPPIA-1086 Download media doesn't show select all option
* OPPIA-1129 Skip toast message tests for API Level 30+
* OPPIA-1037 Update test for build config options

.. _appv96:

v96 (7.3.6) - released 2 Mar 2022
-------------------------------------------------------

Issue list:

* OPPIA-975 Refine error logging
* OPPIA-993 Registration disruption results in starting again
* OPPIA-1021 Create property for displaying REGISTER button
* OPPIA-1007 Fix issue with download course media activity crashing if many
  media
* OPPIA-938/956 Lock topics with password
* OPPIA-1057 Submit quiz attempts in activitylog screen
* OPPIA-1010 Tests for password locking

.. _appv95:

v95 (7.3.5) - released 27 Jan 2022
-------------------------------------------------------

Issue list:

* OPPIA-845 Download media via cell network settings
* OPPIA-936 Update the app course list cache as soon as the user goes to
  download courses
* OPPIA-742 Add option to flush cached courses listing
* OPPIA-900 Add option to prevent display of right/wrong answers at end of quiz
* OPPIA-819 Required registration fields can get hidden by the keyboard
* OPPIA-1019 Video files showing as to download when they have been removed 
  from the course
* OPPIA-916 Check tests which depend on some elements visibility
* OPPIA-953 Reliable running of app automated tests
* OPPIA-662 SonarCloud analysis - get working again


.. _appv94:

7.3.4b (v94) - released 29 Dec 2021
-------------------------------------------------------

Issue list:

* OPPIA-878 Quizzes - for partially correct answers show orange "!"
* OPPIA-492 Refactor deprecated class ActivityTestRule
* OPPIA-917 Review BuildChecksOppiaCore
* OPPIA-902 Restrict access to quizzes with password
* OPPIA-896 Advanced option to download all data from phone

7.3.4a (v93) - released 14 Dec 2021
-------------------------------------------------------

Issue list:

* OPPIA-950 Tracker stats not getting updated after submitting to server

.. _appv92:

v92 (7.3.3) - Released 27 Nov 2021
-------------------------------------------------------

Issue list:

* OPPIA-778 Change text size in course
* OPPIA-849 Continuing to next section on quiz completion
* OPPIA-851 Quiz scores not matching
* OPPIA-830 Some quiz responses get marked as incorrect, when they contain UTF8
  encoded characters
* OPPIA-850 Incorrect layout of some quiz attempts
* OPPIA-891 Fix max number of attempts
* OPPIA-841 Add properties option to be able to turn off gamification 
  notifications by default
* OPPIA-817 Prevent users from editing the notification settings (Build setting)
* OPPIA-801 Send back the course version in trackers
* OPIIA-899 Mismatch on version number display


.. _appv91:

v91 (7.3.2) - Released 29 Oct 2021
-------------------------------------------------------

.. note::
	if the default course reminder options are changed in the custom.properties,
	a Build > Clean might need to be done in Android Studio as for some reason, 
	these can get cached by the gradle build.
 
Issue list:

* OPPIA-797 Gradle upgrade from 4.x to 7.0.3
* OPPIA-715 Add option to edit password and/or full profile
* OPPIA-822 Complete Indicator not working for quiz when threshold is 0
* OPPIA-763 Allow HTML layout in quiz/feedback questions and responses and quiz
  feedback
* OPPIA-812 Protect settings security section with admin password
* OPPIA-783 Allow adding topic icons/images 
* OPPIA-781 Course reminder notifications, allow daily and setting defaults in 
  the app properties file
* OPPIA-813 Video completion not working as expected
* OPPIA-226 Github actions fixes and improvements
* OPPIA-848 Build/config property for allowing delete account


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