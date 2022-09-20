Preserving Activity Identifiers when Updating Content
=======================================================

When activity content is updated a new identifier is generated, as the identifier is the MD5 hash of the activity
content. The rationale for this is so that the specific version of an activity can be identified, and analysis can show
if learners have been using older versions of the content.

The downside to this approach is that any change (even a single character) then generates a new identifier, making it
hard to analyse users activity in content where they may only be very minor changes, for example fixing typos or
phrasing that doesn't really affect the learning content being presented. 

As of :ref:`block version 1.3.5<blockv1.3.5>` you have the option to keep the previous activity identifier. This needs
to be flagged manually since it's not possible for Oppia to know how significant a change is and so whether or not this
should be classed as a new version of an activity, or just a minor update to and existing one.

Where an activity has been updated, as part of the export process you'll be given the option to retain the previous
identifier. 

Criteria
----------

The criteria used for whether you have the option to retain the previous identifier is specific to the activity type:

Page/URL/File activities
^^^^^^^^^^^^^^^^^^^^^^^^^
* Any change in the activity title, description or content

Quiz activities
^^^^^^^^^^^^^^^^
Change the quiz settings

Feedback activities
^^^^^^^^^^^^^^^^^^^


Example cases
-------------

Example Cases A - where you might want to retain the old identifier:

* Fixing minor typo
* New translation of an activity
* Reordering of quiz/feedback questions

Example Cases B - where you will not be given the option to retain the old identifer:

* Change in the number of questions in quiz or feedback activity

Example Cases C - where you would be given the option to retain, but in most cases you should not retain the previous
identifier:

* changes in the learning content, where users do need to be aware that the information in the content is different to
  the previous version
* replacing a question in a quiz or feedback activity, but retaining the same number of questions overall
* changing the settings for a quiz, for example pass threshold, number of attempts allowed, password protection 
* changing the skip logic in a feedback activity
* changing the scoring for a question

The comparison of previous vs updated activity content identifiers doesn't take into account what these changes
specifically are, only that there has been a change. In the example cases C, retaining the previous identifier could
result in:

* Odd results when reviewing quiz responses, for example responses from an old question matching to the new question,
  both in the app (for users) and when exporting/downloading quiz responses from the dashboard (for analytics)
* Different users being scored on different criteria/basis. For example, if user A passes a quiz based on a single
  attempt allowed and a threshold of 80%, then user B passes the quiz when the no attempts allowed are changed and the
  threshold reduced to 50%, but the quiz activity identifier has been retained, then users are not being compared
  like-for-like. This will affect the badge and certificate awarding as well as M&E analysis.


  
Notes
------

* The previous activity identifier is the one that has been pushed to the Oppia server, so it is specific to the
  combination of the Oppia server it has been published with and the status it was published with.


