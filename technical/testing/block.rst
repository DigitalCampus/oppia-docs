Testing Oppia Moodle Export Block
=======================================

.. note::
   Setting up the export block for automated tests is a work in progress.
   
Set up
----------

To be able to run the tests there is some set up you need to do first:

#. Install PHPUnit (https://phpunit.readthedocs.io/) into a ``tools`` directory
   under the block directory
#. Install XDebug (https://xdebug.org/) - this is used for generating the code
   coverage analysis reports
#. Add the XDebug extension to your CLI php.ini file


Running the tests
------------------ 

#. From the Oppia Moodle block ``tools`` directory run::

   ./phpunit ../tests/lib_test.php ../tests --coverage-clover ./coverage.xml --whitelist ../
   
#. To submit the report to SonarCloud, from the Oppia Moodle block directory, run::

	   sonar-scanner \
	   -Dsonar.organization=XXXXXX \
	   -Dsonar.projectKey=XXXXXX \
	   -Dsonar.sources=. \
	   -Dsonar.host.url=https://sonarcloud.io \
	   -Dsonar.login=XXXXXX \
	   -Dsonar.exclusions=.scannerwork/**/*,tests/**/*,tools/**/* \
	   -Dsonar.php.coverage.reportPaths=./tools/coverage.xml
   
   Replacing the organisation, projectKey and login key with your own values for your SonarCloud account

   