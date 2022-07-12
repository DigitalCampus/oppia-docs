OppiaMobile Server Change Log for v0.14.x
=============================================

.. _serverv0.14.2:

v0.14.2 - not yet released
------------------------------------------------------

.. toctree::
   :maxdepth: 2

   upgrading/to_0_14_2

   
Issue list:

* Update Django to 3.2.14

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
 