Setting up Certificates
==========================

.. note::
	Setting up certificates is a work in progress. These docs will be updated as
	we get feedback on this very initial version.
	
	
The Oppia server can automatically generate pdf certificates, which users can
then download to save/print.

How to create certificates for courses
-----------------------------------------

#. Create an image file for your certificate template. This should be a .jpg or 
   .png, 842px wide by 595px high (to match A4 landscape pdf at 72dpi)
#. In your image you can add the borders, layout, logos/text etc. You don't need
   to put in the course title, as the pdf generator can add this, but leave a 
   space for the name.
#. Go to the Django admin pages for your Oppia server, then go to the ``Oppia``
   section and click on ``Certificate Templates``.
#. You can either add a new certificate template, or edit an existing one. Note
   that each course you want to award a certificate for will need it's own image
   file uploaded, but you can upload the same image for multiple courses.
#. When adding a new template, select the badge the certificate is related to
   (will usually be course completed), the course and upload the image file.
#. Until you have the coordinates (eg user name, course title, date etc) lined up
   and outputting correctly on your certificate, leave the certificate template
   disabled, else it will start sending out certificates before you have the
   final settings.
#. From the listing of certificate templates, you click to see a preview/sample.
   If you haven't adjusted any of the other options and coordinates, all the
   data will be printed in the bottom left corner of the certificate.
#. So now we need to decide on which of the 3 data points will be included on
   the certificate (name, course title and date), and adjust the positioning of
   these.
#. Just click to edit the template again, and you can decide which of the three
   data points will appear. For those that you would like to appear, you'll 
   need to edit the corresponding X,Y coordinates.
#. The X, Y coordinates are measured in pixels from the bottom left of the 
   template image, and denotes the bottom middle of where the data point text 
   will appear. So you can use the recommended certificate template image size 
   to help you get started.
#. Likely you'll need to edit these settings and got back to the preview/sample
   a few times until you have all this lined up correctly.
#. Once you are happy with the layout and positioning, you can then enable the
   certificate template. The certificates will start getting generated very
   shortly, and will include creation of certificates for users who had
   previously completed the course.

How are certificates awarded?
-------------------------------

Certificates are created for the selected courses when a user completes the
course and is awarded the badge. So the criteria for getting the certificate is
the same as that for the badge. 

The certificate pdfs are generated and stored on the server, alongside the users
badge. So if the course is updated and/or the certificate template is changed, 
users will retain the certificate at the point in time they were awarded it. 

How do users get their certificates?
---------------------------------------

Currently users can download their certificates from the Oppia server, on their
badges page. But we plan to make the downloadable from the app too.


	
