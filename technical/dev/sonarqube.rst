SonarQube Set Up
==================

There are different ways to set up and use `SonarQube <https://www.sonarqube.org/>`_, 
it's an enterprise level product for analysing source code to maintain code 
quality.

OppiaMobile Server
------------------------

We use the `sonar-scanner <https://docs.sonarqube.org/display/SCAN/Analyzing+with+SonarQube+Scanner>`_ 
tool on the command line to analyse the Oppia server source code and submit the 
results to `SonarCloud <https://sonarcloud.io/dashboard?id=django_oppia>`_.

First we create the test coverage report, using the `Coverage <https://coverage.readthedocs.io/en/latest/index.html>`_ 
tool, using::

	$ coverage erase
	$ coverage run --branch --source=activitylog,api,av,content,gamification,integration,oppia,profile,quiz,reports,summary,viz manage.py test
	$ coverage xml -i
	
Then copy the generated ``django-oppia/coverage.xml`` file into the 
``django-oppia/tests/`` directory.

Then we run the sonar-scanner using::

	/sonar-scanner \
	  -Dsonar.projectKey=django_oppia \
	  -Dsonar.organization=alexlittle-github \
	  -Dsonar.sources=. \
	  -Dsonar.host.url=https://sonarcloud.io \
	  -Dsonar.login=<login id> \
	  -Dsonar.exclusions=docs/_build/**/*,tests/**/*,oppiamobile/settings_secret.py \
	  -Dsonar.python.coverage.reportPath=./tests/coverage.xml

If you are running with your own SonarCloud account, you'll need to use a different projectKey and organisation.
	  
OppiaMobile Android App
------------------------

The Oppia app source code analysis can be found at: https://sonarcloud.io/project/overview?id=DigitalCampus_oppia-mobile-android

To run the analysis for the app, follow these steps:

#. First, you previously need to generate the code coverage. (see: :doc:`../app/code-coverage`).
#. Then, from the root of the app code directory, run::

	./gradlew sonarqube

.. note::
    You will need to set up the secret sonarcloud token for the previous command to work. There are three different ways to do it:

    #. Create an environment variable:

       **SONAR_TOKEN=<your_sonarcloud_token>**


    #. Create a file named sonarqube.properties in the root of the app code directory. Include the following line inside the file:

       **sonar.login=<your_sonarcloud_token>**


    #. Include the parameter in the gradlew command:

       **./gradlew sonarqube -Dsonar.login=<your_sonarcloud_token>**

.. note::
    If you want to generate sonarcloud analysis for your own sonarcloud project, make sure to update sonarqube.gradle file
    so it includes the information of your project.
