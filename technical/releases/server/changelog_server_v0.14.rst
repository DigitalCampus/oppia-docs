OppiaMobile Server Change Log for v0.14.x
=============================================


.. _serverv0.14.11:

v0.14.11 - released 30 Jun 2023
------------------------------------------------------

.. toctree::
   :maxdepth: 2

   upgrading/to_0_14_11

Issue list:

* OPPIA-1543 Add username to quiz & feedback response download file
* OPPIA-1362 Upgrade to Django 4.2, and updates to other libraries
* OPPIA-1423 Update to TastyPie 0.14.5
* OPPIA-1575 Add django command for finding the associated course and acitvity for a specific `quiz_id`

.. _serverv0.14.10:

v0.14.10 - released 27 Apr 2023
------------------------------------------------------

.. toctree::
   :maxdepth: 2

   upgrading/to_0_14_10

Issue list:

* OPPIA-1493 Python library updates
* OPPIA-4 Consistency of: PermissionDenied, Unauthorised and redirect to login
* OPPIA-1368 Update user views permissions check using a mixin
* OPPIA-969/OPPIA-970 Added custom fields in login response and new API endpoint to fetch user data
* OPPIA-1465 Additional API v2 tests to ensure they check all the returned object properties
* Flake8 code formatting updates


.. _serverv0.14.9:

v0.14.9 - released 31 Mar 2023
------------------------------------------------------

.. toctree::
   :maxdepth: 2

   upgrading/to_0_14_9

Issue list:

* OPPIA-1440 Add flake8 config file to use for the code formatting analysis
* OPPIA-983 Fix cognitive complexity in profile/mixins/ExportAsCSVMixin.py
* OPPIA-26: Extracted permissions checks to custom decorator and mixin


.. _serverv0.14.8:

v0.14.8 - released 28 Feb 2023
------------------------------------------------------

.. toctree::
   :maxdepth: 2

   upgrading/to_0_14_8

Issue list:

* OPPIA-1414 Update Django to 3.1.18
* OPPIA-1316 Remove user dropdown selection on cohort participant formset in Django Admin
* OPPIA-1367 Update python/pip packages


.. _serverv0.14.7:

v0.14.7 - released 31 Jan 2023
------------------------------------------------------

.. toctree::
   :maxdepth: 2

   upgrading/to_0_14_7

Issue list:

* OPPIA-1353 Update Python/PIP packages
* OPPIA-1360 Set correct question id when a question is edited
* OPPIA-1362 Store quiz attempt information in data recovery table when an error happens
* OPPIA-1365 Add tests for adding moodle_question_id to feedback questions
* OPPIA-1391 Close media file after use
* OPPIA-1392 Display activity for the current day in the oppia dashboard graphs

Hotfixes:

* OPPIA-1412 Take into account that more than one quizProps can exist
* OPPIA-1414 Fix for downloading media directly from dashboard
* OPPIA-1416 Fix for saving string (not object)
* OPPIA-1422 Create new question if no question exist for a specific moodle_question_id

.. _serverv0.14.6:

v0.14.6 - released 30 Nov 2022
------------------------------------------------------

.. toctree::
   :maxdepth: 2

   upgrading/to_0_14_6

Issue list:

* OPPIA-1331 Prep for upgrading to Django 4
* OPPIA-1341 Fix bug in cohort criteria filtering


.. _serverv0.14.5:

v0.14.5 - released 31 Oct 2022
------------------------------------------------------

.. toctree::
   :maxdepth: 2

   upgrading/to_0_14_5

   
Issue list:

* Upgrade django (to 3.2.16) and other libraries (django-ses, django-sass-processor and reportlab)
* Minor sonarcloud fixes


.. _serverv0.14.4:

v0.14.4 - released 30 Sept 2022
------------------------------------------------------

.. toctree::
   :maxdepth: 2

   upgrading/to_0_14_4

   
Issue list:

* Update library package versions
* OPPIA-1255 Solved Github action failing when it includes a migration
* OPPIA-1257 Update for Google Analytics
* OPPIA-1302 Reordering quiz questions creates duplicate quiz-question pairs in the QuizQuestion DB table


.. _serverv0.14.3:

v0.14.3 - released 31 Aug 2022
------------------------------------------------------

.. toctree::
   :maxdepth: 2

   upgrading/to_0_14_3

   
Issue list:

* Update to Django 3.2.15
* OPPIA-1149 Fix UnorderedObjectListWarning warnings
* OPPIA-959 Fix media download count display
* OPPIA-1264 Fix test failure on upload course with Github workflow actions
* OPPIA-1198 Convert commonly repeated strings to constants
* OPPIA-1161 Add tests for av.views.download_media_file
* OPPIA-1194 Show all dates on daily course activity report
* OPPIA-1083 Generate cohorts based on user profile filters/criteria
* OPPIA-1307 Cohort Creation: Course/Teacher/Student values disappear (HOTFIX 10 Oct 2022)

.. _serverv0.14.2:

v0.14.2 - released 27 Jul 2022
------------------------------------------------------

.. toctree::
   :maxdepth: 2

   upgrading/to_0_14_2

   
Issue list:

* Update Django to 3.2.14 and external libraries
* OPPIA-1121 Enhance cohort capability to make a specific course accessible to only certain user group
* OPPIA-1175 Allow statuses available to be configurable on the server
* OPPIA-1151 Remove sass_processor default_app_config
* OPPIA-1258 Course is published even if the status validation fails
* OPPIA-1261 Can't save cohort if dates not entered


.. _serverv0.14.1:

v0.14.1 - released 30 Jun 2022
------------------------------------------------------

.. toctree::
   :maxdepth: 2

   upgrading/to_0_14_1

   
Issue list:

* Update library package versions for Pillow, openpyxl and xmltodict
* OPPIA-1174 Prevent re-publishing of course depending on status
* OPPIA-1250 Fix for course category API listing
* OPPIA-1251 Fix CleanUpQuizzesTest
* OPPIA-1176 Refactor use of DailyCourseUser and DailyCourseUsers tables/models
* OPPIA-1253 Cron fails if type column in Tracker table is None/Null
* OPPIA-907 Create backup store of unrecognised tracker/quiz data

.. _serverv0.14.0:

v0.14.0 - released 30 May 2022
------------------------------------------------------


.. note::
   This release moves to using Django 3.2
	
.. toctree::
   :maxdepth: 2

   upgrading/to_0_14_0

   
Issue list:

* OPPIA-1144 Upgrade to Django 3.2
* OPPIA-1146 Replace django.utils.translation.ugettext_lazy() with
  django.utils.translation.gettext_lazy()
* OPPIA-1153 Anonymization command, use string type for password
* OPPIA-1152 Replace "ifequal" template tag
* OPPIA-1147 Replace django.conf.urls.url() with django.urls.re_path()
* OPPIA-1148 Replace request.is_ajax() as is deprecated
* OPPIA-1150 Replace Signal(providing_args)
* OPPIA-1158 Remove unused function parameters
* OPPIA-1135 In summary tables in django admin - make view only, prevent
  adding/editing/deletion of rows
* OPPIA-1125 Initial database views
* OPPIA-1165 Simplify how course status is represented
* OPPIA-1167 New read-only status
* OPPIA-1162 Show course link if user can_view_course_activity 
* OPPIA-1166 Media missing event being tracked incorrectly
* OPPIA-1199 Fixes from Sonarcloud analysis
* OPPIA-1173 Add status icons
* OPPIA-1212 Download tracker duplicated


Previous Versions
------------------

.. toctree::
   :maxdepth: 1
   
   changelog_server_v0.13
   changelog_server_v0.12
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
 