Adding quizzes
===============

Add your questions as standard Moodle quiz questions and they will be 
exported to run as quizzes on the mobile device.

The question types supported are:

* Description
* Multichoice (only one valid option)
* Multiselect (one or more valid options)
* True/False
* Matching
* Short Answer
* Numerical



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

Giving Quiz Question feedback
-------------------------------

When you export a course to Oppia, you have the option to specify when question
feedback will appear in the app. The options are:

* After each question and end of quiz
* At the end of the quiz (default)
* Don't show feedback

The Oppia app uses the specific feedback for individual question responses (not
the general feedback), so for quizzes that are part of final assessment 
activities, you might want to be careful about what feedback text you provide, 
and when it is shown.

In the feedback view, depending on the user correct/incorrect responses different icons
are shown:

* Correct answer: green tick (✓)
* Incorrect answer: red cross (❌)
* Partially correct answer: orange exclamation (!).
  Only for multiselect, matching and numerical question types

Quiz password protection
------------------------

The Oppia moodle block offers the possibility of protect the access of a quiz with a password.

If any password is set for a particular quiz, the app will prompt an text box when pressing the "Take this quiz" button.
Only if the correct password is introduced, the user can access this quiz.


HTML Formatting
-----------------

With app version 7.3.2 and above, you can use HTML formatting in your quiz 
questions, quiz responses and question feedback. The following HTML tags are
supported:

p, ul, li, div, span, strong, b, em, cite, dfn, i, big, small, font, blockquote,
tt, a, u, del, s, strike, sup, sub, h1, h2, h3, h4, h5, h6, br

Pass Threshold
----------------


Limiting number of attempts
----------------------------


Password protecting quizzes
----------------------------


Notes on some quiz configurations
-----------------------------------