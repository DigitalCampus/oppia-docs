Database Views
===================

Database views are essentially pre-saved SQL queries, and can help to hide the
database structure complexity. All the actual data comes from other tables, but
these views can be queried and joined in the same way as tables (for ``SELECT``
queries only).

Notes:

* All the views are designed to be helpers only, they will need filtering and
  usually distinct values extracted (due to the user profile fields or other
  property values).
* Users who are listed as staff, admins or who are marked as excluded from
  reporting are already removed from these views.


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

User quiz attempts, linked to user profile fields.

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
* *quizid*
* *quiz_title*
* *quiz_property_name* - courseversion and/or moodle_quiz_id only
* *quiz_property_value* - course version number or moodle_quiz_id number
* *quiz_attempt_date* - date the user attempted the quiz, date is from the
  users device (not the Oppia server)
* *user_score* - score the user achieved
* *quiz_maxscore* - maximum score available for this quiz
* *score_percent* - user score as percentage

