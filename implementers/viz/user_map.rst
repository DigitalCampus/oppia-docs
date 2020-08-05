.. _usermap:

Setting up the User Map Visualization
=====================================

To set up the user map visualization to reflect the your users' location on
your server:

#. Create accounts on:
	  
	  * `ipstack <https://ipstack.com/>`_
	  * `cartodb <https://cartodb.com/>`_
	  
#. Set up a public map/table called `oppiamobile_users` in your CartoDB account
   with the following field names/types:
   
      * lat (number)
      * lng (number)
      * country_code (string)
      * source_site (string)
      * total_hits (number)

#. In the Django admin pages, go to the Settings > Setting Properties model, 
   and update the string values for the following settings, to enter your
   specific API keys etc:

      * `OPPIA_CARBODB_ACCOUNT`
      * `OPPIA_CARBODB_KEY`
      * `OPPIA_IPSTACK_APIKEY`
   		
#. Again, in the Settings, change the `OPPIA_MAP_VISUALISATION_ENABLED` boolean
   value to be `true`
   
#. Create a cron script to run the Django management commands `ip2location` and
   `cartodb_update`. For example::
   
    #!/bin/bash

    cd /home/oppia/
    source env/bin/activate
	
    python ./django-oppia/manage.py ip2location
    python ./django-oppia/manage.py cartodb_update

#. Set up this cron task to run regularly, for example once per day. After the 
   cron task has been run at least once, you should start to see the user 
   locations appearing on the map.  
