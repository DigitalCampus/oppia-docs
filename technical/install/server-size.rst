Server Sizing and Monitoring
=============================

If you have installed the Oppia server from the AWS AMI machine, then you'll
notice this instance size is very small (t2.micro, so is eligible for the 'Free
Tier' on AWS). Whilst this will be fine for some initial testing and setting up,
it won't be suitable for larger scale roll-outs. 

There's not a one-size fits all approach to determining what size of machine is
most appropriate, so below we have given some areas to consider and an example
case of a national roll-out.

Although we specifically mention AWS below, the same or similar will apply to
other cloud server providers. 

To consider
------------

#. How many daily active users are you expecting?

   The number of daily active users is more important to estimate than just the
   raw total number of users you expect to be registered. Since users who are
   registered but not actively using the app will put little or no load on the
   server.
   
#. There will be peaks and troughs in usage levels

   
   
#. Do you have many courses and a lot of video content that users will be
   downloading?

   If you have a lot of courses, and/or a lot of video content that users will
   download, this will put a higher load on the server than the regular activity
   tracking once the users have the courses installed. If you are expecting a
   lot of users to start using the app on the same day, if would be good to
   increase the server size, to ensure they don't have problems registering and
   downloading the courses 
   
#. What sort of promotional activities will you be doing?

   If you are planning promotional activities, think about increasing the server
   size before this promotional activity starts. You can always reduce the
   server size later on, when the activity has slowed down.
 
#. Will you roll out gradually, perhaps to different areas/regions at different
   times?

Example case
-------------------

Here is a real life example, following a national SMS campaign to promote the 
app, giving an idea of the number of users, course downloads and activity hits
in the first few days following the promotion:

* 2000 daily active users
* 10,000 course downloads over 3 days (although most occurring on the launch day)
* 250,000 course activity hits over 3 days

The server size used for this was an AWS m3.xlarge instance (4 vCPUs and 15Gb
RAM), the CPU usage was below 50%.


Server monitoring alerts
--------------------------

We use 2 types of server monitoring:

AWS server monitoring 
~~~~~~~~~~~~~~~~~~~~~~~


AWS CloudWatch:
Status alert checks
CPU over 70%


Updown.io website monitoring
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

We use Updown.io (https://updown.io/) to monitor the Oppia server urls. This is
useful addition to the AWS server monitoring, if (eg) the webserver stops
running, the AWS monitoring would not pick up on this.

Using a physical server
------------------------



Resizing an AWS instance
----------------------------

Changing the size of an AWS instance is straightforward and can be done with a 
few clicks on the AWS Management Console. The main thing to be aware of is that 
the server needs to be turned off whilst changing the server size.

You can view the various instance types available (and pricing) on the AWS site at: 
https://aws.amazon.com/ec2/.

The process is the same whether you are increasing or decreasing the server size.

#. Sign in to the AWS console, at: https://aws.amazon.com
#. Select "EC2" from the management console:
   
   .. image:: images/console.png

#. Select the "availability zone" where your server is installed - for most 
   Oppia server instances this will be EU-West (Ireland), unless you have 
   specifically installed in another zone. Then select 'Instances'

   .. image:: images/select-instances.png
   
   This image shows where you can select the availability zone (top right)
   
#. Select the server you would like to resize, and select "Instance State" > "Stop instance"

   .. image:: images/stop-instance.png
   
#. Once the server is stopped, you can select "Actions" > "Instance Settings" > "Change instance type"

   .. image:: images/change-type.png

#. Select the instance type you would like to change to. Then click "apply"

   .. image:: images/new-type.png

#. Finally start the instance again, go to "Instance State" > "Start instance"

   .. image:: images/start-instance.png

#. Your updated server will be available again in a few minutes.