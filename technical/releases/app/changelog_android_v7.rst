OppiaMobile Android App Change Log v7.x
=========================================


.. _appv81:

v81 (7.1.5) - not yet released - due 1 Nov 2020
-----------------------------------------------

Issue list:

* OPPIA-441 Remove option to download via PC
* OPPIA-257 DbListener redundant
* OPPIA-409 Error when doing release build
* OPPIA-421 Enable making password visible

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