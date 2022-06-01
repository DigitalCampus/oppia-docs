Course Design and Custom Styles
=================================

You can apply custom design/styles to you course content by creating a specific
stylesheet for your course (:ref:`styles`).

The styles can either override a default display style (e.g. for H1, H2 etc). 
Or you can add custom styles, in which case you will need to edit the HTML in 
the Moodle activity.

.. _styles-default: 

Default Styles provided by ``default.css``
------------------------------------------

Definition
~~~~~~~~~~~

HTML::

	<div class="box definition">
	    <p>this means something</p>
	</div>

Display

.. image:: images/style-definition.jpg
	:width: 400 px

Action
~~~~~~~

HTML::

	<div class="box action">
	    <p>you should do this...</p>
	</div>

Display

.. image:: images/style-action.jpg
	:width: 400 px

Warning
~~~~~~~~

HTML::

	<div class="box warning">
	    <p>Lookout!</p>
	</div>

Display

.. image:: images/style-warning.jpg
	:width: 400 px

Info
~~~~~~~~~~~~~~~~

HTML::

	<div class="box info">
	    <p>did you know...?</p>
	</div>

Display

.. image:: images/style-info.jpg
	:width: 400 px
	
Question
~~~~~~~~~

HTML::

	<div class="box question">
	    <p>What proportion of the worldwide number of maternal deaths occurs in Africa?</p>
	    <div name="reveal" id="1" class="reveal">Show answer</div>
	    <div id="answer1">
	        <p>African women account for almost half of the 536,000 women who die every year as a consequence of complications of pregnancy or childbirth.</p>
	    </div>
	</div>

Display

.. image:: images/style-question-closed.jpg
	:width: 400 px

.. image:: images/style-question-open.jpg
	:width: 400 px

Question with inline form input
~~~~~~~~~

This is similar to the previous question type, but it includes an input that requires to be filled by the user to reveal the feedback to the question. The answer introduced by the user is not evaluated for a correct value, the only check is that it is not empty.

For app version ``v7.3.10`` and later, this input values are saved under the ``"data"`` field of the activity tracker.

HTML::

	<div class="box question">
	    <p>This is an inline question</p>
	    <p>With some extra info for that question. Please introduce your answer to reveal the solution</p>
	    <div name="reveal" id="1" class="reveal">
	    	<input type="text"><button>Show answer</button>
	    </div>
	    <div id="answer1">
	    	<p>This is the answer with an explanation</p>
    	</div>
	</div>

Display

.. image:: images/style-inline-question-closed.jpg
	:width: 400 px

.. image:: images/style-inline-question-error.jpg
	:width: 400 px

.. image:: images/style-inline-question-open.jpg
	:width: 400 px

