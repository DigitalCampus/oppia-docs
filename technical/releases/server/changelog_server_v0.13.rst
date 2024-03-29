OppiaMobile Server Change Log for v0.13.x
=============================================


.. _serverv0.13.1:

v0.13.1 - released 2 May 2022
------------------------------------------------------
	
.. note::
   The new course status is not backwards-compatible with previous versions of
   the app (:ref:`v7.3.7<appv97>` and below), so best to avoid actually using
   this new course status until your users have :ref:`app v7.3.8<appv98>` (or
   above). If courses are given the new course status, but users have older
   versions of the app, the course may show as being available to download.
   
.. toctree::
   :maxdepth: 2

   upgrading/to_0_13_1

   
Issue list:

* Update to Django 2.2.28
* OPPIA-1141 Update Python/PIP packages
* OPPIA-1120 Option to flag non-target users
* OPPIA-1112 Allow settings config for cron not running warning
* OPPIA-1071 New course status - unavailable for new install/download
* OPPIA-709 GitHub workflows - able to read/write files for tests
* OPPIA-1124 Update summary tables to enable filtering by user profile fields
* OPPIA-1164 Update quiz summary calculations 
* OPPIA-1186 Fix "expected failing" tests when needing ffmpeg

.. _serverv0.13.0:

v0.13.0 - released 28 Mar 2022 
------------------------------------------------------


.. note::
   This release moves to using Python 3.8, so you will need to follow the
   upgrade instructions below.
	
.. toctree::
   :maxdepth: 2

   upgrading/to_0_13_0

   
Issue list:

* OPPIA-1000 Update to use Python 3.8
* OPPIA-1058 Fix for time taken data report
* OPPIA-973 Add django-storages as server required package
* OPPIA-1074 Add tests for regenerate_course_structure command
* OPPIA-1001 Update Pillow library to 9.0.1 and mysqlclient==2.1.0
* OPPIA-1006 Add automated create/update date fields on profile models
* OPPIA-800 Update the summary_usercoursesummary to record progress in old and
  current versions of the course

Previous Versions
------------------

.. toctree::
   :maxdepth: 1
   
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
 