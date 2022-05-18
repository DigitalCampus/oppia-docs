Preloading Courses and Media
================================

.. note::
	Having courses and media preloaded into your app distribution could 
	significantly increase the size of your app (especially in the case of 
	preloaded media files). Also it means that any updates in the courses or
	media would then require a new app build. Our advice is not to preload
	courses or media unless strictly necessary, instead look at sideloading
	courses and media.

Courses
--------------

If you would like to distribute your app with some courses preinstalled, for 
example if you have a lot of phones you would like set up with the same set of 
courses, then follow these steps:

* Download the course form the Oppia server dashboard (from the specific Oppia
  server the app will be connecting to)
* Place the course zip file(s) in the ``assets/www/preload/courses/`` directory
  (just the unextracted zip file) 
* When the app is installed and run, the courses will be automatically
  installed.

 
 
Media
------------
 
 If you would like to distribute your app with some media preinstalled, then 
 follow these steps:
 
* Place the media file(s) in the ``assets/www/preload/media/`` directory
* When the app is installed and run, the media will be automatically moved to
  the correct directory.
  
From the Oppia server dashboard, you can download a zip file of all the media
needed for a specific course, this ensures you have all the media for the
course, with the correct file names and correct version of the media.
