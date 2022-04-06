Analytics
===========

.. note::
	The options for analytics and reporting are currently being expanded, these
	docs will be updated as this work progresses

Reports
-----------

In addition to the graphs/visualisations that appear on the dashboard homepage,
course and user pages, there is a specific analytics/reports section.


Exporting/Downloading data
-------------------------------

In almost all cases where a graph appears, there is the option to download a 
CSV file of the data that has been used to generate the graph.

For each course, there is a "Course Data Export" option, from here you can 
download (as CSVs) files of all the activity/tracker logs, quiz and feedback 
responses, including previous versions of quizzes and feedback that have been 
in the course.

Custom Analytics/Reporting
---------------------------

For more detailed or custom reporting, it is possible to set up permissions to
connect directly to the SQL database, for example, using a tool such as MySQL
Workbench.

Access for this needs a specific user account creating in MySQL (it's not
connected to your Oppia user account), and also needs some understanding of the
:doc:`database structure </technical/data-structure/index>` to extract 
meaningful and correct data/reports directly from the database.

Users included in the visualisations and reports
--------------------------------------------------

Admin and Staff users are automatically excluded from reports and visualisation
graphs.

As of :ref:`server version 0.13.1<serverv0.13.1>`, specific users can be
flagged to be excluded from some reports and visualisations, for example test
users, project managers etc. If flagged these users will be excluded from the
following (the ones based on data from the CourseDailyStats table):

* Homepage activity graph
* Course homepage activity graph
* Course activity report
* Course downloads report
* Search report

To flag a user to be excluded from these, see 
:ref:`permission-user-exclude-reporting`

