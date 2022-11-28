Export Step 1 - Course Configuration
----------------------------------------

Course Priority
~~~~~~~~~~~~~~~~

To help specify the order in which courses should appear when users go to
download courses in the given tag/category. And also when the course is
displayed in the app main menu listing. For example, if you would like your
courses to display in a particular order in which users should complete them.

Otherwise courses will display in alphabetical order in the app.

Course Categories
~~~~~~~~~~~~~~~~~~~

You must specify at least one category for your course, these are used as the
categories in the app. If no categories are given then users will not be able to
find your course in the app course downloads.

Course default language
~~~~~~~~~~~~~~~~~~~~~~~~

The `ISO-639 code <https://en.wikipedia.org/wiki/ISO_639>`_ that should be used
as the default language for the course content when displayed to users.

.. note::
   In general you do not need to change this from the default ``en`` if your
   course has been set up correctly for multilingual content (see: :doc:`translations`)

Course Sequencing
~~~~~~~~~~~~~~~~~~

By default, this is set to ``none`` so a user will be able to jump around the
course activities however they would like (with the exception of having
completed the pre-test).

To prevent users 'jumping' around in this way, you can force users to complete
the course content either by section/topic (select ``Sequencing within a
section``) or though the whole course (select ``Sequencing through whole
course``).

.. note::
   If your course includes quizzes, and you select ``Sequencing within a
   section`` or ``Sequencing through whole course``, users must get at least
   the quiz pass threshold to be able to progress to the next activity.

Quiz Question Formatting
~~~~~~~~~~~~~~~~~~~~~~~~~~

If your quiz content contains HTML tags for formatting of quiz questions,
response options and question feedback, then select this option. Otherwise all
the HTML formatting will be stripped from the quiz question, response options
and question feedback.

.. note::
   The display of formatted HTML is only supported in version 7.3.2 or higher
   of the Oppia app. If you tick this option and users have a version below
   this, then they will see the HTML tags displayed in the quiz, i.e. <b>Question</b> instead of **Question**.

Thumbnail icon sizes
~~~~~~~~~~~~~~~~~~~~~~

Used to specify the size and dimensions of the icon images that appear in the
app for activities and topics. By default these will be set to 256x256px for
topic icons and 135x90px for activity icons, but these defaults can be changed
in the main block settings.
