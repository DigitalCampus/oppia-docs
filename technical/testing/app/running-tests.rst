Running Tests for OppiaMobile App
=====================================

*OppiaMobile* incorporates several types of tests to make the app stronger.


We have several ways to run tests:

* **Run a single test**:
 
 First, open the class where the test is located, and then right-click the test and click **Run**.

* **Run all tests in a class**:

 Right-click the class you want to test and click **Run**.

* **Run all test classes in a directory**:

 Right-click the directory you want to test and click **Run tests**.

* **Run tests using a test suite**:

 A test suite allows us to run a collection of test that we want. 

 To create a test suite, we need to create a new class and add these tags to the beginning of it:

 .. code-block:: text
  
	  @RunWith(Suite.class)
	  @Suite.SuiteClasses({WelcomeUITest.class, LoginUITest.class, RegisterUITest.class, ResetUITest.class})
	
	  public class UITestSuite {…}


 If we run this suite, the tests inside in the classes listed in ``@Suite.SuiteClasses()`` will be executed.


* **Run all instrumented tests**:

We can create a new debug configuration to run all the instrumented tests within the project. To do so, select the
"Edit configurations" dropdown option, and add a new configuration of type "Android Instrumented tests".
In this new configuration, select to run all tests in Module and pick the `app` module.

.. image:: ../images/instrumented_tests.png

After this, we can select this configuration and run in it in our chosen device.


.. note::

 There is a test which checks the correct behaviour for a successful login so remember to set a valid username and password in the test called: *changeActivityWhenTheCredentialsAreCorrect()* (in LoginUITest.java file)
