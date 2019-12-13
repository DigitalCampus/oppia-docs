OppiaMobile Server Change Log
================================

.. _serverv0.12.3:

v0.12.3 - not yet released
--------------------------------

.. toctree::
   :maxdepth: 1

   upgrading/to_0_12_3
	
Key updates:

* Allow custom fields for profile form
* API for profile updating
* Refactoring of API code
* Lint and SonarCloud fixes

Issue list:

* 697: Fix email sending
  - (`#697 <https://github.com/DigitalCampus/django-oppia/issues/697>`_)
* 692: Add specific test for implementation
  - (`#692 <https://github.com/DigitalCampus/django-oppia/issues/692>`_)
* 645: Emailing password reset not working
  - (`#645 <https://github.com/DigitalCampus/django-oppia/issues/645>`_)
* 682: Update user profile to include custom fields
  - (`#682 <https://github.com/DigitalCampus/django-oppia/issues/682>`_)
* 687: Add API endpoint for user to update their profile info
  - (`#687 <https://github.com/DigitalCampus/django-oppia/issues/687>`_)
* 699: Split out api/resources.py into separate files
  - (`#699 <https://github.com/DigitalCampus/django-oppia/issues/699>`_)
* 605: Remove signup_callback function
  - (`#605 <https://github.com/DigitalCampus/django-oppia/issues/605>`_)
* 660: In tests for file opening use `with ... as ...` instead of file=
  - (`#660 <https://github.com/DigitalCampus/django-oppia/issues/660>`_)
* 700: Course_download_views allows anyone to download any course
  - (`#700 <https://github.com/DigitalCampus/django-oppia/issues/700>`_)
* 684: Remove OPPIA_*_EARN_POINTS settings
  - (`#684 <https://github.com/DigitalCampus/django-oppia/issues/684>`_)
* 709: Upload users function does not work
  - (`#709 <https://github.com/DigitalCampus/django-oppia/issues/709>`_)


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

* 648: Update to django 2.2.x (`#648 <https://github.com/DigitalCampus/django-oppia/issues/648>`_)
* 664: Cohort leaderboard shows empty page (`#664 <https://github.com/DigitalCampus/django-oppia/issues/664>`_)
* 663: Initial version of DHIS2 export (`#663 <https://github.com/DigitalCampus/django-oppia/issues/663>`_)
* 564: In management commands replace print() with self.stdout.write() (`#564 <https://github.com/DigitalCampus/django-oppia/issues/564>`_)

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

* 539: Moving to python 3 and django 2 (`#539 <https://github.com/DigitalCampus/django-oppia/issues/539>`_)
* 468: RemovedInDjango20Warning - update for deprecation/changes (`#468 <https://github.com/DigitalCampus/django-oppia/issues/468>`_)
* 571: For python 3 - replace __unicode__ with __str__ in models (`#571 <https://github.com/DigitalCampus/django-oppia/issues/571>`_)
* 591: Update media_url_check to remove urllib2 dependency (`#591 <https://github.com/DigitalCampus/django-oppia/issues/591>`_)
* 601: Python 3 - v0.12.0 branch - check usage of urllib/urllib2/urllib3 (`#601 <https://github.com/DigitalCampus/django-oppia/issues/601>`_)
* 640: Error with Gamification db migrations on v0.12 branch (`#640 <https://github.com/DigitalCampus/django-oppia/issues/640>`_)
* 577: Drawer menu for admin users (`#577 <https://github.com/DigitalCampus/django-oppia/issues/577>`_)
* 625: Crispy-forms - move to using the BootStrap4 template pack (`#625 <https://github.com/DigitalCampus/django-oppia/issues/625>`_)
* 639: Merge material design branch into latest dev branch (`#639 <https://github.com/DigitalCampus/django-oppia/issues/639>`_)
* 635: Points/gamification not working on staging server with python 3/django 2 (`#635 <https://github.com/DigitalCampus/django-oppia/issues/635>`_)
* 636: Deprecation warning for BaseException.message (`#636 <https://github.com/DigitalCampus/django-oppia/issues/636>`_)
* 638: Fix tests for v0.12.0 branch (`#638 <https://github.com/DigitalCampus/django-oppia/issues/638>`_)
* 649: Date range selector with styles that match the customizable theme (`#649 <https://github.com/DigitalCampus/django-oppia/issues/649>`_)
* 646: Upload view fails if user has no associated UserProfile (`#646 <https://github.com/DigitalCampus/django-oppia/issues/646>`_)
* 650: Add tests for activitylog upload (`#650 <https://github.com/DigitalCampus/django-oppia/issues/650>`_)
* 655: Updates from SonarQube recommendations (`#655 <https://github.com/DigitalCampus/django-oppia/issues/655>`_)
* 585: Add tests for recent updates to activity log (`#585 <https://github.com/DigitalCampus/django-oppia/issues/585>`_)
* 189: Remove CourseXML class as no longer used? (`#189 <https://github.com/DigitalCampus/django-oppia/issues/189>`_)

Previous Versions
------------------

.. toctree::
   :maxdepth: 2
   
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