Custom cohort criteria
===============================================

In some situations, you might want to create a cohort that depends on some custom criteria, for example:

* A cohort that includes all the students from a specific region.
* A cohort that includes all the teachers specialised in a field of knowledge.

In order to add or remove custom criteria in a cohort, an admin or a staff user can do it from the cohorts
page in the dashboard or directly in the admin panel.

.. note::
    For the custom criteria panel to appear in the Django dashboard, there needs to be at least one custom
    user field specified. See: :doc:`Adding extra registration form fields </technical/customise/customfields>`.


The information required for creating a cohort criteria is:

* The **cohort** to which this criteria applies.
* The **role** of the participants (students or teachers).
* **User profile field**: This is the name of the custom user field we want to filter by.
* **User profile value**: The value that the user custom field should have.
  This field accepts comma separated values that will be treated as *OR* operations.

.. note::
    Every custom criteria added for a specific cohort is **additive**, meaning that for a user to be added,
    they should match ALL the criteria.


Updating the cohort participants
--------------------------------------

Once some custom criteria has been added to a cohort, we can update the cohort participants using the custom
actions in the cohorts page from the django admin panel.

These custom actions are:
 #. *Update* cohort participants.
 #. *Refresh* cohort participants.


1. Update cohort participants
_______________________________

When the **Update cohort participants** action is selected, users matching all the criteria will
be added to the corresponding teacher/student role. **No users will be removed, only added.**


2. Refresh cohort participants
________________________________

When the **Refresh cohort participants** action is selected, users matching all the criteria will
be added to the corresponding teacher/student role. **Users who no longer match the criteria will be removed.**