OppiaMobile Server Change Log
================================


.. _serverv0.12.21:

v0.12.21 - not yet released
------------------------------------------------------

.. toctree::
   :maxdepth: 1

   upgrading/to_0_12_21

   
Issue list:

* OPPIA-808 UserNotFound error on exporting trackers
* OPPIA-788 Add server setting to determine if users should be able to edit 
  their profile
* OPPIA-753 Spaces in media filenames can't be played
* OPPIA-803 Monthly active users graph seems awry
* OPPIA-835 Remove some deprecated code for media embed helper


.. _serverv0.12.20:

v0.12.20 - Released 23 Sept 2021
------------------------------------------------------

.. toctree::
   :maxdepth: 1

   upgrading/to_0_12_20

   
Issue list:

* OPPIA-738 Split up update_summaries to different methods
* OPPIA-690 Add category to SettingProperties
* OPPIA-761 Download course can fail if there are very old quiz trackers
* OPPIA-760 Django admin viewing QuizAttemptResponses takes very long time
* OPPIA-711 Management command to remove unused certificate pdfs
* OPPIA-768 Shouldn't regenerate certificate if name is None
* OPPIA-772 Certificate generation issue
* Update Pillow library to 8.3.2
* OPPIA-751 Teachers and normal users get 403 unauthorized when going to 
  courses page



.. _serverv0.12.19:

v0.12.19 - Released 15 July 2021
----------------------------------

.. note::
   *  For the downloading of time spent in courses (#OPPIA-702), the 
      update_summaries command will need to be run from the start - see the 
      upgrading notes
   *  The option to upload media within the dashboard interface, and use the 
      media_embed_code for adding media in Moodle has been removed. All media 
      files should be directly embedded in Moodle.
   * Check permissions for the certificates folder (see full release notes)
   
.. toctree::
   :maxdepth: 2

   upgrading/to_0_12_19

Issue list:

* OPPIA-679 Add option to specify the display name for a certificate
* OPPIA-700 On bulk user upload, add option to include custom registration form
  fields
* OPPIA-693 Add option to regenerate a certificate for a user
* OPPIA-702 Export/accessing time-tracking data
* OPPIA-487 Deprecate media embed helper
* OPPIA-58 Option to register server
* OPPIA-708 Add tests for serverregistation update management task
* OPPIA-680 User profile gives page not found when linking through to an
  archived course
* OPPIA-14 Don't save search tracker if query is blank
* OPPIA-517 On time spent graphs update y-axis to use H:M:S format
* OPPIA-705 Quiz result rounding
* OPPIA-703 Cohort leaderboard doesn't link through to users
* OPPIA-706 Get unauthorised message if teacher user clicks on Cohorts in 
  breadcrumb trail
* OPPIA-406 Server dashboard access log - check all pages covered
* OPPIA-719 Cover the Cohort pages by the dashboard accessed logs
* HOTFIX for update_summaries with timezone


.. _serverv0.12.18:

v0.12.18 - Released 22 Jun 2021
----------------------------------

.. toctree::
   :maxdepth: 1

   upgrading/to_0_12_18
   
.. note::
   The oppiacron task should be run as an admin/sudo user

Issue list:

* Update to Django 2.2.24
* OPPIA-634 Detect if certificate is portrait or landscape - and check correct
  size
* OPPIA-664 Management command to clean media/courses dir
* OPPIA-629 Be able to verify a certificate
* OPPIA-630 Add option to email certificate
* OPPIA-628 Extra tests for certificates
* OPPIA-651 Speed up retrieval of the leaderboard



.. _serverv0.12.17:

v0.12.17 - Released 26 May 2021
----------------------------------

.. toctree::
   :maxdepth: 1

   upgrading/to_0_12_17

Issue list:

* OPPIA-596 Add report for daily course downloads
* OPPIA-622 Initial work for certificates
* OPPIA-638 Pick up email prefix from the app_name
* OPPIA-640 Upgrade required library imports
* OPPIA-591 Allow access to download older versions of quiz and feedback
  responses



.. _serverv0.12.16:

v0.12.16 - Released 25 April 2021
----------------------------------

.. toctree::
   :maxdepth: 1

   upgrading/to_0_12_16

Issue list:

* Update to Django 2.2.20
* Automatically clear expired sessions as part of oppiacron task
* OPPIA-587 API endpoint for username reminder
* OPPIA-584 Improved password reset process
* OPPIA-560 API endpoint to delete account
* OPPIA-557 Add report on inactive users

.. _serverv0.12.15:

v0.12.15 -  Released 26 Mar 2021
----------------------------------

.. toctree::
   :maxdepth: 1

   upgrading/to_0_12_15

Issue list:

* OPPIA-31 Rename 'tags' to be 'categories' to match app and block
* OPPIA-571 Upgrade Django, Pillow and django-ses packages
* OPPIA-343 Explore feedback answers


.. _serverv0.12.14:

v0.12.14 - released 1 Mar 2021
----------------------------------

.. toctree::
   :maxdepth: 1

   upgrading/to_0_12_14

Issue list:

* OPPIA-489 Update to use current approach for loading google charts
* OPPIA-22 No need to show quiz table and quiz info if there are no quizzes in
  the course
* OPPIA-269 Class based views for oppia/course
* OPPIA-268 Class based views for oppia/cohort
* OPPIA-505 Provide course completion badge criteria in server info
* OPPIA-289 API endpoint for getting the course structure
* OPPIA-401 API endpoint to get summary of users course progress

.. _serverv0.12.13:

v0.12.13 -  Released 21 Dec 2020
----------------------------------

.. toctree::
   :maxdepth: 1

   upgrading/to_0_12_13

Issue list:

* OPPIA-496 Add option for giving start/end dates for reports
* OPPIA-497 Add report for search terms used
* OPPIA-502 Additional badge awarding criteria option

.. _serverv0.12.12:

v0.12.12 -  Released 27 Nov 2020
----------------------------------

.. toctree::
   :maxdepth: 1

   upgrading/to_0_12_12

Issue list:

* OPPIA-271 Class based views for integrations
* OPPIA-43 Define constants at module level
* OPPIA-57 UploadMedia - add option for title, organisation and license
* OPPIA-270 Class based views for oppia/home
* OPPIA-467 Report for unique no users, filterable by any customfield definition
* OPPIA-471 Add report for daily active users (initial version)
* OPPIA-437 New export block not including media length (update fix)
* OPPIA-472 Add report for monthly active users (initial version)
* OPPIA-473 add report for total and average time spent
* OPPIA-484 Add option to show only live courses
* OPPIA-266 Class based views for profile/user
* OPPIA-422 Add mocks for testing ip2location and cartodbupdate commands
* OPPIA-194 Testing warning about native datetimes received when timezone
  support is active


.. _serverv0.12.11:

v0.12.11 - Released 27 Oct 2020
----------------------------------

.. toctree::
   :maxdepth: 1

   upgrading/to_0_12_11

Issue list:

* OPPIA-437 New export block not including media length
* OPPIA-451 Add basic Oppia branding to the Django Admin pages
* OPPIA-455 Add data retention script
* OPPIA-458 Management command to remove unused tags
* OPPIA-460 Add quiz management command for quiz difficulty/discrimination
  indices
* OPPIA-461 Update quiz cleanup command

.. _serverv0.12.10:

v0.12.10 - Released 29 Sept 2020
--------------------------------

.. toctree::
   :maxdepth: 1

   upgrading/to_0_12_10

Issue list:

* OPPIA-378 Graphs on summary page showing beginning of month
* OPPIA-412 Publish API can raise `MultiValueDictKeyError`
* OPPIA-413 Summary cron lock doesn't always get removed
* OPPIA-397 Weblink/Intent for opening/downloading a specific course
* OPPIA-414 Create script to anonymise database

.. _serverv0.12.9:

v0.12.9 - Released 26 Aug 2020
--------------------------------

.. toctree::
   :maxdepth: 1

   upgrading/to_0_12_9

Issue list:

* OPPIA-389 Allow downloading of Quiz data in similar way to the feedback
  responses
* OPPIA-381 Badges awarded not always getting added into the UserCourseSummary
  table
* OPPIA-346 Error message when trying to use the makemessages command

.. _serverv0.12.8:

v0.12.8 - released 31 July 2020
--------------------------------

.. toctree::
   :maxdepth: 1

   upgrading/to_0_12_8

Issue list:

* OPPIA-334 If no email is entered when a user registers, it shows ('',) as the
  email address in the Django admin
* Bugfix for Android Intent
* Update Pillow library version
* OPPIA-344 Display the feedback activity responses
* OPPIA-349 Allow course owners to access draft courses

.. _serverv0.12.7:

v0.12.7 - released 1 July 2020
--------------------------------

.. toctree::
   :maxdepth: 1

   upgrading/to_0_12_7
	
Key updates:

* Upgrade to Django 2.2.13

Issue list:

* OPPIA-331 Crash when Admin logs in the first time in a brand new server
  installation
* OPPIA-319 In the download courses, make the course listing appear in the same
  order with the course priority value
* OPPIA-56 UploadMedia - ability to download all media for a course
* OPPIA-342 Search users gives a server error
* OPPIA-369 Course download stats on the course detail page don't match the
  course list
* OPPIA-368 Export of detailed activity to Excel causes error
* OPPIA-5 Set up IPstack for users country locations


.. _serverv0.12.6:

v0.12.6 - released 4 May 2020
--------------------------------

.. toctree::
   :maxdepth: 1

   upgrading/to_0_12_6
	
Key updates:

* bug fixes
* code restructuring for class based views

Issue list:

* OPPIA-281 Add v2 of the API on the server
* OPPIA-285 Store time taken for quiz attempts
* OPPIA-275 Class based views for activitylog
* OPPIA-273 Class based views for content
* OPPIA-18 Cursor error when running summary cron on SQLite db
* OPPIA-200 Graphs on summary page aren't formatted correctly
* OPPIA-264 Class based views for profile/manage
* add django admin search options for some models
* Updated Pillow package
* OPPIA-228 Add API endpoint to return the media embed variables
* OPPIA-260 Show full list of activities and digests for a course
* OPPIA-310 Deleting a user deletes the current account, not the intended one
* OPPIA-318 Occasional issues being unable to download courses in the app - 
  "install failed"

.. _serverv0.12.5:

v0.12.5 - released 18 Mar 2020
--------------------------------

.. toctree::
   :maxdepth: 1

   upgrading/to_0_12_5
	
Key updates:

* Update to Django 2.2.10
* Option to update profile
* Improved configuration options
* Sonarcloud and Django code improvements implemented

Issue list:

* OPPIA-193 Django-GCM package no longer required
* OPPIA-206 Move OPPIA_ALLOW_SELF_REGISTRATION to be bool instead of int
* OPPIA-28 Activity map page configuration
* OPPIA-16 Github actions: new migration
* OPPIA-17 Github actions: static files
* OPPIA-197 Fix the sonarcloud code smells for oppia server
* OPPIA-258 Fix next redirection vulnerability
* OPPIA-241 When downloading a course from the server interface, it doesn't 
  increase the "downloads by users"
* OPPIA-191 Use get_or_created in uploader.py
* OPPIA-262 Class based views for reports
* OPPIA-249 Class based views for av
* OPPIA-13 Remove management command to update short answer scores
* OPPIA-197 Fix the sonarcloud code smells for oppia server
* OPPIA-276 Migrate to using django.urls.path()
* OPPIA-277 Add email field in the LOGIN response
* OPPIA-95 Add option for user to edit their profile - online only



.. _serverv0.12.4:

v0.12.4 - released 29 Jan 2020
--------------------------------

.. toctree::
   :maxdepth: 1

   upgrading/to_0_12_4
	
Key updates:

* update to Django 2.2.9
* additional tests and improved code coverage (85%+)

Issue list:

* 717: Create OppiaTestCase class to be used in tests
  (`#717 <https://github.com/DigitalCampus/django-oppia/issues/717>`_)
* 586: Add tests for quiz/management/commands/check_duplicate_quizzes.py
  (`#586 <https://github.com/DigitalCampus/django-oppia/issues/586>`_)
* 721: Add permissions and tests for the new QuizAttempt/detail views
  (`#721 <https://github.com/DigitalCampus/django-oppia/issues/721>`_)
* 566: Add tests for profile password reset
  (`#566 <https://github.com/DigitalCampus/django-oppia/issues/566>`_)
* 550: SonarQube - complexity of profile/views.py - several functions
  (`#550 <https://github.com/DigitalCampus/django-oppia/issues/550>`_)
* 713: Quiz language dictionaries not being saved correctly
  (`#713 <https://github.com/DigitalCampus/django-oppia/issues/713>`_)
* 710: Add tests for gamification/forms.py
  (`#710 <https://github.com/DigitalCampus/django-oppia/issues/710>`_)
* OPPIA-32 - Move some other settings from settings.py/settings_secret.py to
  SettingProperties

.. _serverv0.12.3:

v0.12.3 - Released 20 Dec 2019
--------------------------------

.. toctree::
   :maxdepth: 1

   upgrading/to_0_12_3
	
Key updates:

* Allow custom fields for profile form
* API for profile updating
* Refactoring of API code
* SonarCloud fixes for duplicate code, code smells and test coverage
* Remove deprecated quiz API endpoints

Issue list:

* 697: Fix email sending
  (`#697 <https://github.com/DigitalCampus/django-oppia/issues/697>`_)
* 692: Add specific test for implementation
  (`#692 <https://github.com/DigitalCampus/django-oppia/issues/692>`_)
* 645: Emailing password reset not working
  (`#645 <https://github.com/DigitalCampus/django-oppia/issues/645>`_)
* 682: Update user profile to include custom fields
  (`#682 <https://github.com/DigitalCampus/django-oppia/issues/682>`_)
* 687: Add API endpoint for user to update their profile info
  (`#687 <https://github.com/DigitalCampus/django-oppia/issues/687>`_)
* 699: Split out api/resources.py into separate files
  (`#699 <https://github.com/DigitalCampus/django-oppia/issues/699>`_)
* 605: Remove signup_callback function
  (`#605 <https://github.com/DigitalCampus/django-oppia/issues/605>`_)
* 660: In tests for file opening use `with ... as ...` instead of file=
  (`#660 <https://github.com/DigitalCampus/django-oppia/issues/660>`_)
* 700: Course_download_views allows anyone to download any course
  (`#700 <https://github.com/DigitalCampus/django-oppia/issues/700>`_)
* 684: Remove OPPIA_*_EARN_POINTS settings
  (`#684 <https://github.com/DigitalCampus/django-oppia/issues/684>`_)
* 709: Upload users function does not work
  (`#709 <https://github.com/DigitalCampus/django-oppia/issues/709>`_)
* 552: SonarQube - complexity of 
  quiz/management/commands/update_short_answer_scores.py handle function
  (`#552 <https://github.com/DigitalCampus/django-oppia/issues/552>`_)
* 587: Duplicate code blocks in quiz management commands
  (`#587 <https://github.com/DigitalCampus/django-oppia/issues/587>`_)
* 548: SonarQube - complexity of oppia/uploader.py - several functions
  (`#548 <https://github.com/DigitalCampus/django-oppia/issues/548>`_)
* 551: SonarQube - complexity of quiz/api/serializers.py format_quiz function
  (`#551 <https://github.com/DigitalCampus/django-oppia/issues/551>`_)
* 547: SonarQube - complexity of oppia/signals.py tracker_callback function
  (`#547 <https://github.com/DigitalCampus/django-oppia/issues/547>`_)
* 712: Quiz API... mainly deprecated?
  (`#712 <https://github.com/DigitalCampus/django-oppia/issues/712>`_)
* 678: Display user full quiz attempts and responses
  (`#678 <https://github.com/DigitalCampus/django-oppia/issues/678>`_)
* 711: Split out oppia/view.py and profile/view.py into separate files?
  (`#711 <https://github.com/DigitalCampus/django-oppia/issues/711>`_)

.. _serverv0.12.2:

v0.12.2 - Released 27 Nov 2019
--------------------------------

.. toctree::
   :maxdepth: 1

   upgrading/to_0_12_2
	
Key updates:

* Additional logging of course publishing
* Updates for PEP8/Flake8 formatting of code
* Add pytest integration with Github workflows
* Remove old/redundant code

Issue list:

* Updated version of Pillow -
  https://github.com/DigitalCampus/django-oppia/pull/669
* 441: Keep log of when a course is republished with the old/new activities -
  (`#441 <https://github.com/DigitalCampus/django-oppia/issues/441>`_)
* 542: Remove OPPIA_EXPORT_LOCAL_MINVERSION setting -
  (`#542 <https://github.com/DigitalCampus/django-oppia/issues/542>`_)
* 676: Add tests for quiz attempts in activity log upload -
  (`#676 <https://github.com/DigitalCampus/django-oppia/issues/676>`_)
* 680: Check that the server can be set up with SQLite as the db - 
  (`#680 <https://github.com/DigitalCampus/django-oppia/issues/680>`_)
* 512: Remove GCM push/device admin functionality
  (`#512 <https://github.com/DigitalCampus/django-oppia/issues/512>`_)
* 685: Add pycodestyle to requirements
  (`#685 <https://github.com/DigitalCampus/django-oppia/issues/685>`_)
* 672: Find out why media views showing as 0
  (`#672 <https://github.com/DigitalCampus/django-oppia/issues/672>`_)
* 683: Replace raw_input() with input()
  (`#683 <https://github.com/DigitalCampus/django-oppia/issues/683>`_)
* 688: Configure github workflow yml file
  (`#688 <https://github.com/DigitalCampus/django-oppia/issues/688>`_)
* 666: Make left hand side bar collapsible
  (`#666 <https://github.com/DigitalCampus/django-oppia/issues/666>`_)
* 692: Add specific test for implementation
  (`#692 <https://github.com/DigitalCampus/django-oppia/issues/692>`_)
* 667: test_quiz_attempt_points_included test failing
  (`#667 <https://github.com/DigitalCampus/django-oppia/issues/667>`_)
  

.. _serverv0.12.1:

v0.12.1 - Released 15 Oct 2019
--------------------------------

.. toctree::
   :maxdepth: 1

   upgrading/to_0_12_1
	
Key updates:

* Updated version of Django
* Initial version of DHIS2 export

Issue list:

* 648: Update to django 2.2.x 
  (`#648 <https://github.com/DigitalCampus/django-oppia/issues/648>`_)
* 664: Cohort leaderboard shows empty page
  (`#664 <https://github.com/DigitalCampus/django-oppia/issues/664>`_)
* 663: Initial version of DHIS2 export
  (`#663 <https://github.com/DigitalCampus/django-oppia/issues/663>`_)
* 564: In management commands replace print() with self.stdout.write()
  (`#564 <https://github.com/DigitalCampus/django-oppia/issues/564>`_)

.. _serverv0.12.0:

v0.12.0 - Released 17 Sept 2019
--------------------------------

.. toctree::
   :maxdepth: 1

   upgrading/to_0_12_0

Key updates:

* Moving to Python 3 and Django 2
* Use material design layout

Issue list:

* 539: Moving to python 3 and django 2
  (`#539 <https://github.com/DigitalCampus/django-oppia/issues/539>`_)
* 468: RemovedInDjango20Warning - update for deprecation/changes
  (`#468 <https://github.com/DigitalCampus/django-oppia/issues/468>`_)
* 571: For python 3 - replace __unicode__ with __str__ in models
  (`#571 <https://github.com/DigitalCampus/django-oppia/issues/571>`_)
* 591: Update media_url_check to remove urllib2 dependency
  (`#591 <https://github.com/DigitalCampus/django-oppia/issues/591>`_)
* 601: Python 3 - v0.12.0 branch - check usage of urllib/urllib2/urllib3
  (`#601 <https://github.com/DigitalCampus/django-oppia/issues/601>`_)
* 640: Error with Gamification db migrations on v0.12 branch
  (`#640 <https://github.com/DigitalCampus/django-oppia/issues/640>`_)
* 577: Drawer menu for admin users
  (`#577 <https://github.com/DigitalCampus/django-oppia/issues/577>`_)
* 625: Crispy-forms - move to using the BootStrap4 template pack
  (`#625 <https://github.com/DigitalCampus/django-oppia/issues/625>`_)
* 639: Merge material design branch into latest dev branch
  (`#639 <https://github.com/DigitalCampus/django-oppia/issues/639>`_)
* 635: Points/gamification not working on staging server with python 3/django 2
  (`#635 <https://github.com/DigitalCampus/django-oppia/issues/635>`_)
* 636: Deprecation warning for BaseException.message
  (`#636 <https://github.com/DigitalCampus/django-oppia/issues/636>`_)
* 638: Fix tests for v0.12.0 branch
  (`#638 <https://github.com/DigitalCampus/django-oppia/issues/638>`_)
* 649: Date range selector with styles that match the customizable theme
  (`#649 <https://github.com/DigitalCampus/django-oppia/issues/649>`_)
* 646: Upload view fails if user has no associated UserProfile
  (`#646 <https://github.com/DigitalCampus/django-oppia/issues/646>`_)
* 650: Add tests for activitylog upload
  (`#650 <https://github.com/DigitalCampus/django-oppia/issues/650>`_)
* 655: Updates from SonarQube recommendations
  (`#655 <https://github.com/DigitalCampus/django-oppia/issues/655>`_)
* 585: Add tests for recent updates to activity log
  (`#585 <https://github.com/DigitalCampus/django-oppia/issues/585>`_)
* 189: Remove CourseXML class as no longer used?
  (`#189 <https://github.com/DigitalCampus/django-oppia/issues/189>`_)

Previous Versions
------------------

.. toctree::
   :maxdepth: 1
   
   changelog_server_v0.11
   changelog_server_v0.10
   changelog_server_v0.9
   changelog_server_v0.8
   changelog_server_v0.7
   changelog_server_v0.6
   changelog_server_v0.5
   changelog_server_v0.4
   changelog_server_v0.3
   changelog_server_v0.2
   changelog_server_v0.1