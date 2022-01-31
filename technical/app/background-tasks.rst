OppiaMobile App Background Tasks
====================================

This page explains when various background tasks will run and what they actual
do. The task names are specifically listed using their java class names (under 
the ``org.digitalcampus.oppia.task`` package).

Note this page only covers tasks that run automatically in the background, not 
tasks that are triggered by user generated events (eg registering, logging in
etc).

CourseInfoTask
--------------------------

*Purpose*: to get the updated list of new, updated and deleted courses

*Trigger/s to run*: Runs couple of times a day in the background, can also be 
run manually from the advanced settings (flush course cache)


ScanMediaTask
-----------------

*Purpose*: to check if the user has all the course media on their device

*Trigger/s to run*: Runs when opening the app on the app homepage, and on the 
course index pages


SubmitQuizAttemptsTask
----------------------------

*Purpose*: to send unsubmitted quiz attempts to server

*Trigger/s to run*: runs automatically every 6 hours


SubmitTrackerMultipleTask
-----------------------------

*Purpose*: to send unsubmitted activity logs to server

*Trigger/s to run*: runs automatically every 6 hours


UpdateLeaderboardFromServerTask
-----------------------------------

*Purpose*: to update the leaderboard

*Trigger/s to run*: when the leaderboard is opened


