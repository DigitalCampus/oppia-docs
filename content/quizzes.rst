Adding quizzes
===============

Add your questions as standard Moodle quiz questions and they will be 
exported to run as quizzes on the mobile device.

.. contents::
	:depth: 2

Question types supported
----------------------------

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

The Oppia moodle block offers the possibility of protect the access of a quiz 
with a password.

A password can be set in the Moodle quiz settings, under the 
``Extra restrictions on attempts`` section.

If any password is set for a particular quiz, the app will prompt an text box
when pressing the "Take this quiz" button. Only if the correct password is 
introduced, the user can access this quiz.


HTML Formatting
-----------------

With app version 7.3.2 and above, you can use HTML formatting in your quiz 
questions, quiz responses and question feedback. The following HTML tags are
supported:

p, ul, li, div, span, strong, b, em, cite, dfn, i, big, small, font, blockquote,
tt, a, u, del, s, strike, sup, sub, h1, h2, h3, h4, h5, h6, br

Pass Threshold
----------------

On export from the Oppia block you can set the pass threshold for each quiz 
(from 0-100%, default is 80%). The pass threshold determines the mark a user 
must achieve to have the quiz being considered completed/passed.


Limiting number of attempts
----------------------------

On export from the Oppia block you can set the maximum number of attempts a user
can have at a quiz (1-10 or unlimited, default is unlimited).


Notes on some quiz configurations
-----------------------------------

#. If a quiz has the max no attempts set, and has a pass threshold higher than 0,
   then if a learner uses up all their attempts, but still hasn't passed the 
   quiz, then there's no way for them to complete/pass the course.
#. In the instance above, this can be made worse if the course sequencing is set,
   as then there's also no way for a user to access the rest of the topic/course.