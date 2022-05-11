Database Views
===================

Database views are essentially pre-saved SQL queries, and can help to hide the
database structure complexity. All the actual data comes from other tables, but
these views can be queried and joined in the same way as tables (for ``SELECT``
queries only).


reports_viewusercoursecompletepercent
-------------------------------------

User course completion data, linked to user profile fields.

Columns:

* *id* - id number from user profile field 
* *userid*
* *username*
* *first_name*
* *last_name*
* *email*
* *phone_number*
* *profile_field_name* - user profile field name
* *profile_field_value_int* - integer user profile field value
* *profile_field_value_str* - string user profile field value
* *profile_field_value_bool* - boolean user profile field value
* *course_id*
* *course_title*
* *no_activities_completed* - number of activities the user has completed,
  based on the ``completed_activities`` column in
  :ref:`summary_usercoursesummary`
* *total_no_activities* - total number of activities in the current version of
  the course
* *percent_complete* - percentage based on ``no_activities_completed`` and
  ``total_no_activities``

.. note::
   Calculating the total_no_activities (and hence percent_complete) column,
   causes the view to be very slow.

reports_viewuserquizscores
--------------------------