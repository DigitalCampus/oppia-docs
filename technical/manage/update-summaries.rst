Running Update Summaries in background
==========================================

Running the ``python manage.py update_summaries --fromstart`` can take a very long time, hours for implementations with
large amounts of activity logs. So in most cases, when fully rebuilding the summary cache tables, it's good to run this
in the background, so you can log out of the terminal and leave running (eg overnight).

There are lots of different ways this can be done, but the method we usually use is to use the ``nohup`` command.

When the python virtual environment is enabled, run::

	nohup python manage.py update_summaries --fromstart &

You can then log out of the terminal and the task will continue to run. To check the progress, you can run::

	 cat nohup.out
	 
to see the output. After the task has succesfully finished you can delete the nohup.out file, if it's left in the 
filesystem the next time nohup is run, then output will get appended to this file (not replaced).

If you see a message that "Oppia cron is already running" or similar, then likely the cron task is already running, or
it has aborted abnormally (eg due to server reboot).

To allow running again, you will need to remove either the ``oppia_cron_lock`` and/or the ``oppia_summary_cron_lock``
from the Django admin pages, under the Settings model.