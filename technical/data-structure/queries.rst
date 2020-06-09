Sample queries for extracting data
======================================

Responses for quiz or feedback activity
---------------------------------------------

.. code-block::

	SELECT qq.id, qq.title, qqu.title, qqar.text, qqa.user_id FROM quiz_quizattempt qqa 
	INNER JOIN quiz_quizattemptresponse qqar ON qqa.id = qqar.quizattempt_id 
	INNER JOIN quiz_quiz qq ON qqa.quiz_id = qq.id
	INNER JOIN quiz_question qqu ON qqar.question_id = qqu.id
	WHERE qqa.quiz_id in (17,18,20,22,24,26);

The ``where`` clause specifies the id numbers of the quiz/feedback you would
like to extract the data for.

