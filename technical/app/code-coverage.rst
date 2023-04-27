
Generating App Code Coverage
==============================

#. Start an android emulator.
#. Run the following gradle task::

    ./gradlew jacocoTestReport

   **Note:** This task runs all the app tests and it will take some time to finish, please be patient.

#. When the previous task is finished and all tests succeeded, the coverage report will be located at *'oppia-mobile-android/app/build/report/coverage'*
