Updating Content
==================================


Whilst a course for an Oppia implementation is being developed, and before the
app in launched, course content can be updated and published to the server as
often as is necessary.

However, once a course has been launched, and is being used by learners,
publishing updates should be well planned and coordinated. Firstly to reduce
the burden and potential confusion to users for having a lot of small, regular
updates and secondly, to ensure a good review can be made of the content before
it is made live for learners.

There are different options for updating course content, depending on the
version of the block you are using:

* If you are using the Oppia Export Block below v1.1.1 (so the version number is
  not shown in the bottom of the block), please refer to: 
  :doc:`updating-old-block`
* If you are using the Oppia Export Block v1.1.1 or above (the version number is
  shown at the bottom of the block), pease refer to: :doc:`updating-new-block`


What happens to learner progress when a course is updated?
------------------------------------------------------------

When a course is updated, any activities that have been changed (in any way, 
from a minor typo, to a rewrite), the old version of the activity is 
essentially 'detached' from the new version of the course. Although note that 
if option B above is used for updating, then all activities will be seen as new.

Any deleted activities are also just detached, and any new activities are just 
added. The tracker and quiz scores etc are retained.

From a user perspective on their device, when they download the new version:

* if they haven't yet completed the old version of the activity, there's no
  real difference to them
* if they completed the old version of the activity, but not completed the 
  course, the updated version of the activity will now show as no longer
  completed
* if they have already completed the course and got the badge, then they will
  keep the badge, but the updated version of the activity will now show as no
  longer completed

