Adding feedback
=================

You can use the standard Moodle feedback activity to create feedback questions
in Oppia.

The feedback question types supported are:

* multichoice
* info
* label
* textarea 
* description
* multichoicerated
* numeric

In the Oppia app the feedback questions use the same question types and format
as the quiz content, except without the scoring and marking.

Applying skip logic
--------------------

As of :ref:`block version 1.3.1<blockv1.3.1>` and :ref:`app version 7.3.7<appv97>`
you can add skip logic to feedback activities, eg to show a follow up question 
if the user gave a particular response to a previous question.

In Moodle you can define this using the ``dependence item`` and ``dependence
value`` fields on the feedback question.

.. note::
   If you deploy a course that has skip logic in the feedback activities, but
   users have an older version of the app (i.e. below 7.3.7), then they will
   see all the questions as the skip logic will not be applied in the app. So
   before adding skip logic to your feedback activities you should ensure that
   all users will have app v7.3.7 or above.

Restricting number of submissions
----------------------------------

Courses published using :ref:`block version 1.3.4<blockv1.3.4>` or earlier will always allow multiple attempts at any
feedback activities.

From :ref:`block version 1.3.5<blockv1.3.5>` onwards, you can use the "allow multiple submissions" setting in the Moodle
feedback activity to allow or prevent multiple submissions. 

.. note::
   After updating to :ref:`block version 1.3.5<blockv1.3.5>` or above, if the course was previously published to Oppia,
   and you want to retain the option for allowing multiple submissions, you will need to set this in Moodle before
   republishing the course, since Moodle's default is to only allow a single submission.
