Embedding Files in Page Activities
========================================

.. note::
    Embedding files in page activities is only supported from :ref:`oppia-export-block verion 1.4.4<blockv1.4.4>` and 
    for users with :ref:`app version 7.4.5<appv110>` or above. See additional info below for previous app versions.
    
In addition to adding file activities, you can also embed files (e.g. pdfs) directly in page activities. 
The type of files supported by the Moodle export block is handled by extension type. Currently only ``.pdf`` are included.

How to embed a file
----------------------

#. First of all, you have to embed the resource file in the page activity. To do so, on the page content you are editing use the "Manage files" button in the Moodle page text editor:
   
   .. image:: images/manage-files.png
   
   Then select the "Upload a file" option and upload it to the page content.

#. Now you just need to create an internal link to the file that was just embedded. If you want an icon to represent the link to the file, you can upload an image representing the file type or a thumbnail of the contents, using the "Insert image button" as with any embedded image into page contents.

#. Once you have the content to display, just need to create a link to the embedded file. To do so, select the image (and posible caption) and click on the "Link" button of the Moodle text editor.
   
   .. image:: images/file-insert-link.png

   On the dialog that appears, instead of manually introducing a URL, click on the "Browse repositories" button, and a dialog will appear to let you select the element you want this link to lead

#. On the link dialog, click the "Embedded files" tab on the lateral menu, and select the file you included in the first step.
   
   .. image:: images/file-picker-embedded.png

With this, the OppiaMobile block will handle the internal link to the file and include it in the course package during the export process. 


Recommendations
------------------

#. Not all file types can be opened in a default Android installation and require an additional app. E.g. a pdf file
   requires a pdf reader to be available on the device, and a PowerPoint will require an additional app for user to open
   on their devices. Before embedding files into pages, you should check that users will have the appropriate app to
   open the file.
#. Some document file types may be difficult to read on a small screen, involving horizontal and vertical scrolling. You
   should check how the files will display on your users devices, so they are easily usable.
#. If the embedded file is text heavy, it may be more appropriate to move this text to being directly in the page
   activity, rather than an external embedded file.
#. Embedded files will count towards the total file size of your course, so if you are including large files (or a lot
   of embedded files in a course), you may want to consider reviewing how usable this will be for your users. 



Activity completion
---------------------

By default, embedding a file in a page activity will then require the user to at least have opened the file for the page
activity to be considered as having been completed. You can change this default behaviour at app build level, by modifying the property
`PAGE_COMPLETION_VIEW_FILE` (see :doc:`../technical/customize/app/settings` )

On unsupported app versions
-----------------------------

For users with :ref:`app version 7.4.4<appv109>` or below, if they try to open an embedded file they might not be able
to open the PDF file (specially with Android versions 11 or higher, where the external app management permissions changed. 

In this cases, a message will appear inside the contents below the link to the resource file stating the
minimum version required for this functionality to work correctly.

   .. image:: images/file-compat-message.png

Note that in the case where opening the file is required to completed the page
activity, this criteria won't apply for users with old app versions.
