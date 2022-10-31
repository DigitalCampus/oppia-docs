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

.. code-block:: shell

    curl -sS https://getcomposer.org/installer | php
    php composer.phar update


2. Install Behat
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: shell

    php composer.phar require --dev behat/behat


3. Install Mink extension
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
`Mink <https://mink.behat.org/en/latest/>`_ is an open source browser controller/emulator for web applications, written in PHP.

.. code-block:: shell

    php composer.phar require --dev behat/mink
    php composer.phar require --dev behat/mink-extension
    php composer.phar require --dev behat/mink-goutte-driver
    php composer.phar require --dev behat/mink-selenium2-driver

4. Create dataroot folder for Behat
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Create a new dataroot folder for Behat. It is recommended that you create this folder in the same directory as your *moodledata* folder.
You can name this folder anyway you like, but a recommended name is *moodledata_behat*.


5. Update config.php
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

6. Initialise Behat
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: php

    php admin/tool/behat/cli/init.php

7. Add MOODLE_ROOT environment variable
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: shell

    export MOODLE_ROOT=<your_moodle_installation>


8. Run the oppia_mobile_export block tests
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
1. Start a Selenium standalone server

    .. code-block:: shell

        cd oppia_mobile_export/tests/lib
        java -jar selenium-server-4.5.3.jar standalone &

2. Run the features

    .. code-block:: shell

        # From the root folder of your moodle installation
        ./vendor/bin/behat --config <path to moodledata_behat>/behatrun/behat/behat.yml --tags=@block_oppia_mobile_export

    .. note::

        The option :code:`--tags=@block_oppia_mobile_export` will run all the *.feature* files that include the tag
        **@block_oppia_mobile_export**.

Writing new Behat features
-------------------------------

You should locate all new features in *oppia_mobile_export/test/behat*. Behat will run all .feature files located in that folder.
For extending an existing feature, create a new *Scenario* clause in the feature file.


HTML Report and Code Coverage
-------------------------------

When the Behat tests have finished, two new folders should have been created:

- **tests/behat/report**: This folder contains the HTML report of the Behat run. Open the index.html file in your browser to see it.
- **tests/behat/CodeCoverage**: This folder contains the code coverage report in HTML format.