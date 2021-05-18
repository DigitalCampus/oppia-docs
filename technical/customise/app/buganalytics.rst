Automated Bug Reporting and Analytics
=======================================

There are many automated bug tracking and analytics services/plugins that you 
can use to monitor the performance of your implementation of Oppia app, and we
have tried to make it straightforward for you to add the specific tool that you 
would prefer to use. Perhaps you are already using one for other app and you 
would like to use the same one for Oppia.

By default, the Oppia app will be set up without an automated bug tracking or
analytics service configured.

We already have helper classes set up for integrating Count.ly or Splunk Mint
bug reporting set up. How to confgiure these is described below, along with how
you can add other helper classes for other systems.

Count.ly
------------

Count.ly (https://count.ly/) is a bug reporting and analytics tool that has an
open source Community Edition, so you can install and run on your own servers.

To use Count.ly in Oppia all you need to do is add the following to your 
``custom.properties`` file (with the appropriate server and app key)::

	ANALYTICS_LIBRARY=COUNTLY
	COUNTLY_SERVER_URL=https://<url-to-your-countly-server>
	COUNTLY_APP_KEY=<your-countly-app_key>

Splunk Mint
--------------

.. note::
	From the end of Dec 2021, Splunk Mint will no longer be maintained, and is 
	due to be replaced by a new product from Splunk, although, at the time of 
	writing, full details of the new product have not been made available. 
	Therefore it is recommended not to use Splunk Mint for new implementations 
	of Oppia.
	
To use Splunk Mint in Oppia all you need to do is add the following to your 
``custom.properties`` file (with the appropriate api key)::

	ANALYTICS_LIBRARY=MINT
	MINT_API_KEY=<your-api_key>

Adding another plugin/service
-------------------------------

You can add other bug/analytics platforms by adding an new class in the 
``org.digitalcampus.oppia.analytics`` package that extends the ``BaseAnalytics`` 
class and overrides the appropriate methods.

You will almost certainly also need to add ``BuildConfig`` parameters in the 
``build.gradle`` file and add the specific values in your ``custom.properties`` 
file. For example, for API keys or URLs for your bug/analytics tool.
