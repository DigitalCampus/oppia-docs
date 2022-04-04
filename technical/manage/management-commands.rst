OppiaMobile Server Management Commands
=========================================

Django's manage.py runs a variety of Django admin tasks. OppiaMobile bundles 
some specific management commands for the management of the Oppia server.

To run any of this commands, just use the ``manage.py`` script like with the 
common Django admin actions (i.e. activating the virtualenv and setting your 
path to the server folder).

To view all the commands available in any Django project, you can type 
``manage.py help`` to view a list of them, grouped by Django app. Also, you can 
access the help for a command typing ``manage.py help <command_name>``.

Some commands are run automatically (by the oppia cron), and others must be 
manually from the command line, this is indicated below if a command is auto or 
manual.

[oppia] ``anonymize`` (manual)
---------------------------------
**Anonymises the database**. Removes all personal information (profile info, 
passwords, IP addresses, user agents etc) from the database. This is useful when 
needing to use a copy of a live database for testing/bug fixing, but do not want 
(or need) to share the live personal information. This can only be run if the 
Oppia server is in debug mode.

[oppia] ``clean_categories`` (manual)
--------------------------------------
**Removes unused categories**. I.e. those that don't have any courses attached 
to them.

[oppia] ``clean_certificates`` (manual)
----------------------------------------
**Removes old certificate pdf files**. If certificates have been regenerated, 
this can leave the old pdf in the file system, this command will remove these 
unused/obsolete certificates.

[oppia] ``cleanup_uploads`` (manual)
--------------------------------------
**Cleans up any old files in the oppia uploads directory**. Cleans the temporary 
zip files uploaded to the server that are no longer needed. It also checks that 
every course in the server has its related course package so it can be 
downloaded, printing a warning for each of them that doesn't satisfy this.


[oppia] ``data_retention`` (manual)
--------------------------------------
**Removes user profiles and activity based on data retention policy**. Removes 
user accounts and activity from the database if the user hasn't logged in or had 
any activity in the last X years. The default no years is 7, but can be changed
in the :ref:`system-config-settings` .


[oppia] ``generate_certificates`` (auto or manual)
----------------------------------------------------
**Creates pdf certificates for users who have completed courses**. It will also 
email certificates to users if this has been enabled 
(:ref:`certification-settings`). When run manually, you can regenerate all the 
certificates (eg if the template has changed), or for a specific user (eg if 
their name was spelled incorrectly).


[oppia] ``oppiacron`` (auto)
--------------------------------------
**Core oppia cron task**. Runs the other management commands that need to be run 
regularly (eg generate_certificates) and also awards badges.


[oppia] ``populate_courseversion`` (manual)
------------------------------------------------
**Populates the course_version field in the tracker model based on the current 
course activities**
As of :ref:`server version 0.12.22<serverv0.12.22>` the course version will 
automatically be recorded, this script is to backfill the course versions for 
activities submitted before the server was upgraded to this version.


[oppia] ``regenerate_course_structure`` (manual)
------------------------------------------------
**Regenerates the course structure from the course upload file XML**
Only necessary to use if it looks like the course activities have got out of
sync.


[oppia] ``remove_duplicate_trackers`` (manual)
------------------------------------------------
**Removes any duplicate trackers based on UUID**


[quiz] ``backfill_moodle_ids`` (manual)
-----------------------------------------
**Backfills Moodle quiz and question ids into the Oppia database**.

As of :ref:`block version 1.3.0<blockv1.3.0>` Moodle quiz and question are
automatically exported to be included as quiz and question properties in the
Oppia database.

However, course that were exported prior to this version of the block being
installed will not then have the Moodle quiz and question ids included in the
Oppia database. If these id number are needed for courses that were published
previously, then you can use this management command as follows:

#. Export the course again from Moodle, but no need to publish to Oppia (if the
   course is otherwise unchanged), just download the generated course zip file
#. Extract the module.xml file from the course zip file, and place in a folder
   on the Oppia server
#. Run this management command: ``python manage.py backfill_moodle_ids <path>/module.xml`` 

[quiz] ``cleanup_quizzes`` (manual)
--------------------------------------
**Cleans up old quizzes and questions that are not relevant anymore**.
It removes all the quizzes and its related data (properties, questions, correct 
answers, etc) that are not part of a course anymore and don't have any attempt. 
Before actually deleting the data, the command prompts the user for confirmation.

[quiz] ``question_analysis`` (manual)
--------------------------------------
**Generates the difficulty and discrimination index** for each question in the
given quiz
        
[quiz] ``remove_duplicate_quiz_attempts`` (manual)
---------------------------------------------------

**Removes any duplicate quiz attempts based on instance_id**


[serverregistration] ``update_server_registration`` (auto)
-----------------------------------------------------------
**Updates the server registration information** if the Oppia server is 
registered with https://implementations.oppia-mobile.org   
 
[summary] ``update_summaries`` (auto)
--------------------------------------

**Updates course and points summary/cache tables**. Usually this is run 
automatically, but can also be run manually if a full cache rebuild needs to be 
done.

[viz] ``cartodb_update`` (auto or manual)
--------------------------------------------
**Updates the user location map** in `CartoDB <http://cartodb.com/>`_
:ref:`More information <usermap>` about how to set up and configure the location
map	

[viz] ``ip2location`` (auto or manual)
--------------------------------------

**Converts the IP addresses from the Tracker log to a latitude/
longitude location**, for displaying on the CartoDB user map visualization.
:ref:`More information <usermap>` about how to set up and configure the location
map
    
   




	


