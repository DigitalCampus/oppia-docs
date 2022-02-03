Creating your course in Moodle
===============================

If we have set up a course area for you on our Moodle server, then here are some 
basic instructions to help get you started. If you would like to request us to 
set up an area in Moodle for you to test out your course in OppiaMobile please 
`contact us <mailto:alex@digital-campus.org>`_.

You should have received by email your username, password and link to your 
course area.

If you're creating a course on your own Moodle server, it is likely best to use
the "Topics" format for your course.

When you're on the course homepage press the 'turn editing on' button in the top
right then you get the options to add/edit activities/resources etc - for media 
essentially you'll need to just to create "page resources". 

For information about specific aspects of course creation for OppiaMobile, see:

.. toctree::
   :maxdepth: 1
   
   guidelines
   activitytypes
   images
   quizzes
   video_embed
   topic_locking
   custom_styles
   feedback
   translations
   about
   testing
   publish_to_oppia 

Once you have some content etc that you'd like to test on your phone, press the 
'Export to Oppia Package' button in the right hand column. At the end of the 
export output page, if it's all exported successfully, there will be a link to 
download the course .zip package. So you can download this and copy it to the 
``/<storage_setting>/Android/data/org.digitalcampus.mobile.learning/files/download`` 
directory. The storage_setting path will depend on where you have the app 
storage location set to.

Then when you start up the OppiaMobile app on your phone it will automatically 
install the course and you can see how it all looks on your phone/tablet.

Once you're happy with how it all looks on your phone, you can upload the course 
to our server (http://demo.oppia-mobile.org - same username/password that you 
use for the OppiaMobile client app) and it'll be available for anyone to 
download. 

.. note::
	Information on :ref:`how to include stylesheets and javascript<styles>` 
	in your course

If you have any queries, comments or suggestions on how to improve these
instructions, the course authoring process or any other aspect of OppiaMobile, 
please post them in the `OppiaMobile Community site <https://community.oppia-mobile.org/>`_ 