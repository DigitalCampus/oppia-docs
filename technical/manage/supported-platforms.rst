Supported Platforms
========================

Oppia depends on external operating systems, programming languages and platforms. When new versions of these are
released there usually need to be updates to the Oppia platform components to ensure they are compatible with the latest
versions.

The current versions of operating systems, platforms etc that Oppia supports is listed below. Other platforms, OSs etc
may work, but these are not ones that we have specifically tested with, so you might come up against errors, bugs if you
are using these.


Oppia Android App
-------------------

.. raw:: html
   :file: android-versions.html


Oppia Server
--------------

.. raw:: html
   :file: python-versions.html
   
Notes:

* We run Oppia on Ubuntu LTS releases (currently 22.04) with MySQL 8.x, other database systems and
  operating systems that are supported by Django should also function correctly (assuming a supported Python version is
  being used), however you should check yourself.
* Upgrading Ubuntu to another version (eg 23.04) might automatically change the default Python version used, so take
  care before doing significant OS updates.

Moodle - Oppia Export Block
----------------------------

.. raw:: html
   :file: moodle-versions.html
   
Notes:

* As with the Oppia server, we run Moodle on Ubuntu LTS releases. Updating to another version of Ubuntu may cause the
  default PHP version to also be updated, so again, take care when doing significant OS updates