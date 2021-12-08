Sideloading Content onto Devices
=================================

To prevent needing to download courses and media files from directly in the app 
(using wifi or mobile data connection), courses and media files can be 
`sideloaded` onto devices. This means connecting the mobile device to laptop or 
computer and directly copying the files from there onto the mobile device.

The base directory on the mobile device to copy content into is (eg):

``/sdcard/Android/data/data/org.digitalcampus.mobile.learning/files/``

The exact path will depend on whether the app is set up to store content on 
internal or external storage, and also the specific package name of your app. 

Sideloading courses
------------------------

Firstly download the course zip file directly from the live Oppia server. The 
course needs to have been published as a live course on the live server, and be
a final version.

Copy the course zip file into:

``/sdcard/Android/data/data/org.digitalcampus.mobile.learning/files/download/``

There is no need to unzip the file.

When the app is next opened on the mobile device the course will be installed.

Sideloading media content
----------------------------

Firstly download the media files from the live Oppia server:

* Go to the Oppia server dashboard
* Go to the specific live course page
* Click on ``Related media``
* Download the zip file of the media for the course
* Unzip the downloaded media file on your laptop/computer

Copy the media files into:

``/sdcard/Android/data/data/org.digitalcampus.mobile.learning/files/media/``

Directory permissions on mobile devices
------------------------------------------

More recent versions of Android (eg v11+) might prevent direct access to the app
data folders. This is a security feature Google has built into Android to 
prevent apps being able to access data from other apps.

So you might need to install a specific file manager (eg 
https://play.google.com/store/apps/details?id=com.lonelycatgames.Xplore&hl=en_US&gl=US) 
to be able to access the app specific directories on Android 11+
