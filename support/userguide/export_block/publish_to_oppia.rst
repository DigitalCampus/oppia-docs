Publishing your Moodle Course to Oppia
========================================

When you have completed :doc:`/content/author`, or at least, are ready to test your course in the OppiaMobile app, then
you will need to publish your course to the OppiaMobile server.

From the OppiaMobile Export Block in your Moodle course:

#. Select the ``connection`` you would like to use (see below: 
   :ref:`export_server_connections_explained`).
#. Select the ``Course design`` you would like to use.
#. Select the ``Course status``, either ``Draft/testing`` or ``Live``
#. Press the ``Export to Oppia Package`` button.
#. On the next page, you will see some options for quizzes and general course settings


.. _export_server_connections_explained:

Server Connections - Explained
-----------------------------------

There is not a 1-1 connection between a particular Moodle course and an 
OppiaMobile server. A Moodle course could be published to several OppiaMobile 
servers, and conversely, an OppiaMobile server could host courses from 
different Moodle servers.

So when you export a course from Moodle to OppiaMobile, you need to specify 
which OppiaMobile server you want to export to.

If you do not see the OppiaMobile server you'd like to export to, then you'll 
need to ``Add a new server connection``, providing:

#. Server name - this is just your reference 
#. The url to the OppiaMobile server
