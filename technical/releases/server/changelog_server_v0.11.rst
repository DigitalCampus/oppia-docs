OppiaMobile Server Change Log for v0.11.x
==========================================



.. _serverv0.11.1:

v0.11.1 - Released 25 Jun 2019
--------------------------------

.. toctree::
   :maxdepth: 1

   upgrading/to_0_11_1

Key updates:

* Documentation moved to its own repository: https://github.com/DigitalCampus/oppia-docs
* Interface for customising the points for individual activities

Issue list:

* 600: On about page use download link from the server settings - https://github.com/DigitalCampus/django-oppia/issues/600
* 596: Update acknowledgement page/s - https://github.com/DigitalCampus/django-oppia/issues/596
* 529: Review and complete code process docs - https://github.com/DigitalCampus/django-oppia/issues/529
* 606: Add QA checklist and template - https://github.com/DigitalCampus/django-oppia/issues/606
* 607: Update links to digital-campus/oppiamobile - https://github.com/DigitalCampus/django-oppia/issues/607
* 608: Update links to community site - https://github.com/DigitalCampus/django-oppia/issues/608
* 603: Review the requirements.txt and look at using some of the more recent versions - https://github.com/DigitalCampus/django-oppia/issues/603
* 598: static/oppia/style.css file now redundant - https://github.com/DigitalCampus/django-oppia/issues/598
* 572: Update/review docs for how the offline registration works - https://github.com/DigitalCampus/django-oppia/issues/572
* 593: Make email and phone no optional on registration - https://github.com/DigitalCampus/django-oppia/issues/593
* 602: Move the docs to their own repository - https://github.com/DigitalCampus/django-oppia/issues/602
* 619: Gamification - for the course global point check it doesn't read from the baseline custom points - https://github.com/DigitalCampus/django-oppia/issues/619
* 616: Add events/points to the Gamification db tables - https://github.com/DigitalCampus/django-oppia/issues/616
* 615: Editing points for individual activities - https://github.com/DigitalCampus/django-oppia/issues/615
* 614: Check that all gamification points are loaded from the defaults - https://github.com/DigitalCampus/django-oppia/issues/614
* 617: Update the course version no when the points are updated - https://github.com/DigitalCampus/django-oppia/issues/617
* 619: Gamifcation - for the course global point check it doesn't read from the baseline custom points - https://github.com/DigitalCampus/django-oppia/issues/619
* 613: course_xml_reader.py no longer used - https://github.com/DigitalCampus/django-oppia/issues/613
* 620: Add labels and helper text for the gamification elements - https://github.com/DigitalCampus/django-oppia/issues/620
* 621: Remove the QuizGamificationEvent table - doesn;t need to be used - https://github.com/DigitalCampus/django-oppia/issues/621
* 626: Move default points to being in their own DB table - https://github.com/DigitalCampus/django-oppia/issues/626
* 620: Add labels and helper text for the gamification elements - https://github.com/DigitalCampus/django-oppia/issues/620
* 622: Rewrite custom gamification points when course is updated/republished - https://github.com/DigitalCampus/django-oppia/issues/622
* 628: Customize gamification points in a single view - https://github.com/DigitalCampus/django-oppia/issues/628
* 637: Error when publishing via API - https://github.com/DigitalCampus/django-oppia/issues/637
* 645: Emailing password reset not working - https://github.com/DigitalCampus/django-oppia/issues/645
* 634: Fix issue with AYRH course on live server (`#634 <https://github.com/DigitalCampus/django-oppia/issues/634>`_)
* 644: When publishing a course, get permissions error (`#644 <https://github.com/DigitalCampus/django-oppia/issues/644>`_)

.. _serverv0.11.0:

v0.11.0 - Released 20 Mar 2019
--------------------------------

.. toctree::
   :maxdepth: 1

   upgrading/to_0_11_0

	
Key updates:

* Upgrading to Django 1.11.20
* Restructuring of project to match Django best practice
* Extra automated tests
* Improved documentation structure and updates

Issue list:

* 486: Refactor django project structure - https://github.com/DigitalCampus/django-oppia/issues/486
* 495: Use CDN versions of js libraries rather than local copies - https://github.com/DigitalCampus/django-oppia/issues/495
* 492: Update leaderboard pagination display to match the courses - https://github.com/DigitalCampus/django-oppia/issues/492
* 389: Implement "Open activity in app" functionality - https://github.com/DigitalCampus/django-oppia/issues/389
* 490: Use LESS/SASS for better frontend development - https://github.com/DigitalCampus/django-oppia/issues/490
* 488: Update to use Bootstrap 4 - https://github.com/DigitalCampus/django-oppia/issues/488
* 519: Update to Django 1.11.15 - https://github.com/DigitalCampus/django-oppia/issues/519
* 521: Add a 'contributing.md' file - https://github.com/DigitalCampus/django-oppia/issues/521
* 523: Remove the 'mobile' & 'preview' directories - https://github.com/DigitalCampus/django-oppia/issues/523
* 534: Error on publishing course, due to project restructuring - https://github.com/DigitalCampus/django-oppia/issues/534
* 504: In Ubuntu 18.04 avprobe is replaced with ffprobe - https://github.com/DigitalCampus/django-oppia/issues/504
* 536: Update to Django 1.11.18 - https://github.com/DigitalCampus/django-oppia/issues/536
* 535: Add tests for publishing courses and media files using the API - https://github.com/DigitalCampus/django-oppia/issues/535
* 532: Database migration fails on 0012_fix_future_tracker_dates.py - https://github.com/DigitalCampus/django-oppia/issues/532
* 537: Add tests for the uploading media (via the webform) - https://github.com/DigitalCampus/django-oppia/issues/537
* 543: Add tests for editing user profile (via form) - https://github.com/DigitalCampus/django-oppia/issues/543
* 544: SonarQube - complexity of profile/views.py edit function - https://github.com/DigitalCampus/django-oppia/issues/544
* 553: SonarQube - complexity of viz/views.py summary_view function - https://github.com/DigitalCampus/django-oppia/issues/553
* 516: Update docs for installing - with the new project structure - https://github.com/DigitalCampus/django-oppia/issues/516
* 505: Investigate options for less reliance on specific command line tools - https://github.com/DigitalCampus/django-oppia/issues/505
* 538: Update platform architecture/workflow docs - https://github.com/DigitalCampus/django-oppia/issues/538
* 489: Restructure documentation - https://github.com/DigitalCampus/django-oppia/issues/489
* 477: MIDDLEWARE_CLASSES deprecation during installation - https://github.com/DigitalCampus/django-oppia/issues/477
* 494: Badges page is not linked to from anywhere? - https://github.com/DigitalCampus/django-oppia/issues/494
* 559: Add tests for profile urls - https://github.com/DigitalCampus/django-oppia/issues/559
* 560: Add tests and data for viz models and functions - https://github.com/DigitalCampus/django-oppia/issues/560
* 557: Unusual start date on the summary overview - https://github.com/DigitalCampus/django-oppia/issues/557
* 526: Review and update server settings page - https://github.com/DigitalCampus/django-oppia/issues/526
* 525: Remove development_server setting and use debug instead - https://github.com/DigitalCampus/django-oppia/issues/525
* 530: Move cron and cronsummary tasks to be under the oppiamobile directory? - https://github.com/DigitalCampus/django-oppia/issues/530
* 364: Logging when cron was last run - https://github.com/DigitalCampus/django-oppia/issues/364
* 375: Implement cron lock - https://github.com/DigitalCampus/django-oppia/issues/375
* 565: Copy the OPPIA_ALLOW_SELF_REGISTRATION setting.py into SettingProperties - https://github.com/DigitalCampus/django-oppia/issues/565
* 558: Add upgrade docs to v0.11.0 - https://github.com/DigitalCampus/django-oppia/issues/558
* 297: Docs for export process from Moodle to Oppia - https://github.com/DigitalCampus/django-oppia/issues/297
* 561: Add app settings to docs - https://github.com/DigitalCampus/django-oppia/issues/561
* 496: Improve how email templates are handled - https://github.com/DigitalCampus/django-oppia/issues/496
* 563: Remove oppia/cron.py and move it to the management command oppiacron.py - https://github.com/DigitalCampus/django-oppia/issues/563
* 576: Use the db settings for storing/editing the ip2location and cartodb_update usernames, api_keys - https://github.com/DigitalCampus/django-oppia/issues/576
* 533: Styling with BootStrap 4 - https://github.com/DigitalCampus/django-oppia/issues/533
* 555: Cohort add/edit form doesn't show the list of available teachers/students - https://github.com/DigitalCampus/django-oppia/issues/555
* 575: TypeError: 'Tracker' object has no attribute '__getitem__' - https://github.com/DigitalCampus/django-oppia/issues/575
* 554: Cohort add/edit form has some layout issues - https://github.com/DigitalCampus/django-oppia/issues/554
* 573:  Update/review docs for how the bluetooth transfer works - https://github.com/DigitalCampus/django-oppia/issues/573
* 574: Update/review docs for how the activity log transfer works - https://github.com/DigitalCampus/django-oppia/issues/574
* 579: Media viewed not being displayed correctly - https://github.com/DigitalCampus/django-oppia/issues/579
* 580: Course download points being left out - https://github.com/DigitalCampus/django-oppia/issues/580
* 581: Quiz attempt points being added twice - https://github.com/DigitalCampus/django-oppia/issues/581
* 590: Quiz points added twice - from tests - https://github.com/DigitalCampus/django-oppia/issues/590
* 592: Move to Django 1.11.20 on v0.11.0 branch & master - https://github.com/DigitalCampus/django-oppia/issues/592
* 570: Make sure use of COURSE_UPLOAD_DIR always uses os.path.join() - https://github.com/DigitalCampus/django-oppia/issues/570

