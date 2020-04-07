Adding quizzes
===============

Add all your questions as standard Moodle quiz questions and they will be 
exported to run as quizzes on the mobile device. Note that only questions which 
can be marked automatically can be exported, so any essay questions will not be 
exported as these require manual marking. 

Essentially the question types supported are:

* any question supported by the `Moodle GIFT format <http://docs.moodle.org/28/en/GIFT_format>`_ (with the 
  exception of essay) can be exported to OppiaMobile
* Drag and drop questions are also supported


Randomising questions
----------------------

Often you won't want users to see the same questions in the same order every 
time they attempt a particular quiz. With Moodle and Oppia, you can set up a
group of questions and specify how many of these questions will be randomly 
selected each time a user attempts a quiz. To do this:

* In your quiz in Moodle, add all of the questions you want the randomised
  selection to be from
* When you export to Oppia, you can select the number of questions that will
  be randomly selected each time the user attempts the quiz (see 
  :ref:`export_options_explained`)

Creating pre-tests
--------------------

For creating a pre-test that users must complete in the Oppia app before they
can access the course content, create your quiz in the 'Topic 0' section of 
your Moodle course (i.e. before any other topics/sections).
