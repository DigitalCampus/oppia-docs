Testing OppiaMobile
======================

OppiaMobile incorporates several types of tests to make the app and server 
stronger and make sure updated code does not break existing functionality.

For the core components of OppiaMobile, we use the SonarCloud code analysis tool
to help us measure and improve the maintainability of the code and the automated
test coverage. The current Sonarcloud analysis reports can be found at:

* Oppia Server: https://sonarcloud.io/dashboard?id=django_oppia
* Oppia App: https://sonarcloud.io/dashboard?id=org.digitalcampus.mobile.learning
* Moodle to Oppia Export Block: https://sonarcloud.io/dashboard?id=DigitalCampus_moodle-block_oppia_mobile_export

The processes for running the existing tests, and also how to add new tests, is 
described below:


.. toctree::
   :maxdepth: 2
   
   app/running-tests
   app/adding-tests
   app/notifications
   server
   block
   
   
If you have problems or failures when running or creating tests, then please 
contact us via the `OppiaMobile Community <https://community.oppia-mobile.org/>`_