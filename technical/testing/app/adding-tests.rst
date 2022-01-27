Creating new tests for OppiaMobile App
========================================

*OppiaMobile* incorporates several types of tests to make the app stronger.

These types of tests are **Local Unit Tests**, **Instrumented Tests** and **User Interface Tests**.


Local Unit Tests
-------------------
The Local Unit Tests are tests that run on a local JVM, therefore we do not need a physical device or emulator to run this type of tests, which make the execution time to be shorter.

The main path for these tests is ``src/test/java``. It is mandatory for this type of tests to include the JUnit 4 framework dependency to the app *build.gradle* file.

.. code-block:: text

   testImplementation 'androidx.test.ext:junit:{version}'
 
The tests methods that we create must have the tag ``@Test`` right before the method declaration, and must end with an **assertion** to check whether the test passes or not. For example:
 
.. code-block:: text

   @Test
   public void Storage_correctDownloadPath(){
        …
        assertTrue(downloadPath.isCorrect());
   }
 

Optionally, the tests could provide a preconditions and post conditions blocks

.. code-block:: text

 //Preconditions block

 @Before
 public void setUp() throws Exception{…}



.. code-block:: text

 //Post-conditions block

 @After
 public void tearDown() throws Exception{…}


Instrumented Unit Tests
-------------------------

The Instrumented Unit Tests are test that run on a physical device or emulator. This type of tests is convenient when we need access to instrumentation information (App context for example).

The main path for this tests is ``src/androidTests/java``.

To create and run this test, first we need to install the **Android Support Repository** from the *Android SDK Manager*. After that, we need to add some dependencies to the app *build.gradle* file:

 
.. code-block:: XML

    androidTestImplementation 'androidx.annotation:annotation:{version}'
    androidTestImplementation 'androidx.test:runner:{version}'
    androidTestImplementation 'androidx.test:rules:{version}'
    androidTestImplementation 'androidx.test.ext:junit:{version}'
    androidTestImplementation 'androidx.test.uiautomator:uiautomator:{version}'
    androidTestUtil 'androidx.test:orchestrator:{version}'

In addition, we need to add the default test instrumentation runner to use JUnit 4 test classes, and its parameters:

.. code-block:: XML
 
 android {
     defaultConfig {
        testInstrumentationRunner "androidx.test.runner.AndroidJUnitRunner"
        testInstrumentationRunnerArguments clearPackageData: 'true'
        testInstrumentationRunnerArguments coverage: 'true'
        testInstrumentationRunnerArguments coverageFilePath: '/sdcard/coverage/'
     }
    ...

    testOptions {
        execution 'ANDROIDX_TEST_ORCHESTRATOR'
        unitTests.returnDefaultValues = true
        unitTests.includeAndroidResources = true
        animationsDisabled = true
    }
 }

When we create a test class, there are some things we have to pay attention.

* We need to add the ``@RunWith(AndroidJUnit4.class)`` tag before the test class definition.
 
* We also need to add the ``@Test`` tag to all our test methods (as we did in the *Local Unit Tests* section) 
 
* The ``setUp()`` and ``tearDown()`` methods have the same structure as in the *Local Unit Tests* section.
 
* All our tests methods should include the **throws Exception** line in the method definition.
 
* The assertion part is the same as in the *Local Unit Tests* section.

User Interface Tests
-----------------------
 
The User Interface Tests are useful to verify that the UI components of the app works correctly and do not provide a poor experience to the final user.

*OppiaMobile* make use of these tests using the **Espresso** testing framework, that we might consider it as an Instrumentation-based framework to test UI components. 

With *Instrumentation-based* we mean that it works with the **AndroidJUnitRunner** test runner (as mention in the previous section).

To use the Espresso library, we need to make sure to follow the same steps described in the previous section (Instrumented Unit Tests) and also we need to add the following dependency to the app *build.gradle* file:


.. code-block:: XML
 
 androidTestImplementation 'androidx.test.espresso:espresso-core:{version}'



* The *Espresso* nomenclature is based on three aspects. First we need to **find the view** we want to test. Next, we have to **perform an action** over that view. And finally, we need to **inspect the result**. This is done as follows:

 .. code-block:: java

    onView(withId(R.id.login_btn))		        //Find the view
        .perform(click());		            //Perform an action
    onView(withText(R.string.error_no_username))	//Find the view
        .check(matches(isDisplayed()));       //Inspect the result

Mock Web Server
-----------------

*OppiaMobile* made use of the **MockWebServer** by *okhttp* (https://github.com/square/okhttp/tree/master/mockwebserver).

The mock web server is useful to enqueue some responses and in this way testing the client side.

First, we need to add the MockWebServer dependency to our app *build.gradle* file:

.. code-block:: XML
 
    testImplementation 'com.squareup.okhttp3:mockwebserver(insert latest version)’


After that, we are able to create MockWebServer objects. For example:



.. code-block:: text
 
    MockWebServer mockServer = new MockWebServer();
	
    String filename = “responses/response_201_login.json”; //Premade response

    mockServer.enqueue(new MockResponse()
        .setResponseCode(201)
        .setBody(getStringFromFile(InstrumentationRegistry
            .getInstrumentation().getContext(), filename)));
	
    mockServer.start();


On the other hand, we need to configure our app to communicate correctly with this mock web server. To achieve that, *OppiaMobile* uses the class ``MockApiEndpoint``, whose method ``getFullURL()`` will give us the correct path on which the mock web server is listening.


Temporary Files and Folders
-----------------------------

**Junit4** allows us to create temporary files and folders with the guarantee that it will delete all of them when the test finishes, whether the test passes or fails.

The ``TemporaryFolder`` object must be created using the ``@Rule`` tag.

.. code-block:: text
 
    @Rule
    public TemporaryFolder folder = new TemporaryFolder();
	
    //Use
    File tempFolder = folder.newFolder(“tempFolder”);
    File tempFile = folder.newFile(“tempFile.txt”);


Considerations to create consistent tests
-----------------------------------------

- When testing screens with ViewPager, if we swith page with smooth scroll, sometimes the test try to handle next event before the transition finishes, so it fails. The quik solution is to add a wait time in the test just after page transition event: Thread.sleep(200) -200ms is enought-. Other solution would be to add an Idling resource but it is not compatible with ViewPager and we'd need to replace with ViewPager2 and its adapter.

- | Espresso waits until AsyncTasks finish if there is a UI change at the end (onPostExecute). If we need to test the result after a AsyncTask wihout UI change (i.e. only saves data), we need to add a wait time. In slow devices, this could take more than a second so Thread.sleep(3000) should be enought.

- To test properties which configure UI elements, first add tests to check desired element visibility in UIChecksPropsBased, and then we have to mock the property value in the rest of the tests it is involved. If the property is no mockeable (it is not included in the Settings so it has no preference associated), just exit the test (i.e. we cannot test anything related with Settings if MENU_ALLOW_SETTINGS is disabled)

- Remember to to close soft keyboard after typing text if we need to click any button (keyboard could hide UI elements and make the test fail as they are not clickable). I.e.: onView(withId(R.id.edit_email)).perform(typeText("any@email.com"), closeSoftKeyboard());

- If inside a Activity/Fragment there is a repository object with any async process in it, and a ProgressDialog (or similar) is created while the process finishes, there is risk of not closing the ProgressDialog if the repository method (which contains the async process) is mocked and test will fail as there is a not expected view at top. The solution would be to move the code with creates the ProgessDialog inside the repository method or ensure we call the "onComplete" method mocking it in the test with doAnswer(invocationOnMock -> ....)


**DEVICE CONFIGURATION BEFORE RUNNING THE TEST:**

- Disable system animations: Settings -> Developer options -> disable: Window animation scale, Trasition animation scale and Animator duration scale
- Disable any auto-fill service: Settings -> Languages and input -> Auto-fill service
- Some soft keyboards could modify layout behaviour. Ensure the default one is selected (not accessibility or custom): Settings -> Languages and input -> Virtual keyboard
- Set English language


**In addition, if the testing device is phisical device:**

- Set Airplane mode to avoid incoming push notifications (system UI notifications could hide part of the screen and make the tests fail)
- Disable screen rotation

