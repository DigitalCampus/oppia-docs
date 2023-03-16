Behat
=========

.. note::
   This documentation page is in progress and might suffer modifications.

`Behat <https://docs.behat.org/en/latest/>`_ is an open source Behavior-Driven Development framework for PHP.
Behat features are writen in `Gherkin <https://en.wikipedia.org/wiki/Cucumber_(software)#Gherkin_language>`_, which is a
human readable language for writing (and at the same time documenting) test cases. A simple example to undestand the Gherkins syntax:

.. code-block:: gherkin

   Feature: Refund item
    Scenario: Jeff returns a faulty computer
      Given: Jeff has bought a computer for $900
      And: he has a receipt
      When: he returns the computer
      Then: Jeff should be refunded $900


Local Set Up
------------------

1. Install composer
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

To install the Behat dependencies will rely on Composer. Composer is a tool for dependency management in PHP. It allows you to declare the libraries your project depends on and it will manage (install/update) them for you.

Check the `Composer documentation <https://getcomposer.org/doc/00-intro.md>`_ on how to install and configure it in your development environment.


2. Install Behat and Mink extension
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Under the root folder of your Moodle installation, run the following to install Behat:

.. code-block:: shell

    composer require --dev behat/behat


`Mink <https://mink.behat.org/en/latest/>`_ is an open source browser controller/emulator for web applications, written in PHP.

.. code-block:: shell

    composer require --dev behat/mink
    composer require --dev behat/mink-extension
    composer require --dev behat/mink-goutte-driver
    composer require --dev behat/mink-selenium2-driver
    composer require --dev dvdoug/behat-code-coverage

3. Create dataroot folder for Behat
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Create a new dataroot folder for Behat. It is recommended that you create this folder in the same directory as your *moodledata* folder.
You can name this folder anyway you like, but a recommended name is *moodledata_behat*.


4. Update local configuration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
1. Open the config.php file located in your moodle root location.
2. Search for the line :code:`require_once(__DIR__ . '/lib/setup.php');`
3. Paste the following code **before** the line indicated in the previous step:

    .. code-block:: php

        $CFG->behat_dataroot = '/path/to/the/dataroot/you/created';
        $CFG->behat_wwwroot = 'http://127.0.0.1/path/to/your/site';
        $CFG->behat_prefix = 'beh_';

4. Replace the property :code:`$CFG->wwwroot` if necessary:

    .. code-block:: php

        //Make sure you use localhost here instead of 127.0.0.1
        $CFG->wwwroot = 'http://localhost/path/to/your/site';

    .. note::

        **About behat_wwwroot**

        You will need to set the :code:`$CFG->behat_wwwroot` to your Moodle site, but it **must** use a different
        value to your :code:`$CFG->wwwroot`.

        One common way to do this is to use :code:`127.0.0.1` for behat, but :code:`localhost` for standard use.
        Alternatively you can add an additional hostname in your :code:`/etc/hosts` file and use this instead.


5. Initialise Behat
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Next, we need to initialise the Behat testing environment, and create the tests site. For this, we first are going
to 

First, you need to clone the :code:`moodle-browser-config` repository in the root folder of your Moodle instalation:


After the repository is succesfully downloaded, we need to add it as a requirement in the :code:`config.php` file 
before the line  :code:`require_once( __DIR__ . '/lib/setup.php')` :

.. code-block:: php

    require_once( __DIR__ . '/moodle-browser-config/init.php');


Then, we can run the Behat script to create the test environment and site:

.. code-block:: php

    php admin/tool/behat/cli/init.php

Be patient, this process can take a while. After it completes succesfully, a message like the following will
appear:

.. code-block:: shell

    Acceptance tests environment enabled on http://127.0.0.1/moodle, to run the tests use: 
    vendor/bin/behat --config /var/moodledata_behat/behatrun/behat/behat.yml


6. Add MOODLE_ROOT environment variable
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: shell

    export MOODLE_ROOT=<your_moodle_installation>


7. Run the oppia_mobile_export block tests
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

### Using Selenium

1. Start a Selenium standalone server

    .. code-block:: shell

        cd oppia_mobile_export/tests/lib
        java -jar selenium-server-4.5.3.jar standalone &

2. Run the features

    .. code-block:: shell

        # From the root folder of your moodle installation
        ./vendor/bin/behat --config blocks/oppia_mobile_export/tests/behat/behat.yml


### Using Geckodriver (Firefox)

1. Start the geckodriver server

    .. code-block:: shell

        geckodriver

2. Run the features

    .. code-block:: shell

        # From the root folder of your moodle installation
        ./vendor/bin/behat --config blocks/oppia_mobile_export/tests/behat/behat.yml --profile=geckodriver


Writing new Behat features
-------------------------------

You should locate all new features in *oppia_mobile_export/test/behat*. Behat will run all .feature files located in that folder.
For extending an existing feature, create a new *Scenario* clause in the feature file.


HTML Report and Code Coverage
-------------------------------

When the Behat tests have finished, two new folders should have been created:

- **tests/behat/report**: This folder contains the HTML report of the Behat run. Open the index.html file in your browser to see it.
- **tests/behat/CodeCoverage**: This folder contains the code coverage report in HTML format.