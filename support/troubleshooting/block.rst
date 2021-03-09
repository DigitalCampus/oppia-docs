Troubleshooting Moodle Oppia Export Block
===========================================


Warning about missing "poster" image for media element
---------------------------------------------------------

This will occur if you do not specify a poster image for a media file that you
have put in your content.

The video can still be played in the app, only that users will only see a text
link to start the video, rather than an image.

To remove this warning, you should go back to edit the activity and media file
to add a poster image, see: :doc:`../../content/video_embed`


Duplicated digest error
----------------------------

This will occur if you have identical activities in the same course. The digest
is an identifier based on the activity title and content, if the activity title
and content is identical for 2 or more activities in the course you will get
this error message and be unable to export the course.

If it was an error to repeat the same activity, then go back to the course and
remove the duplicated activity.

If it was deliberate that there are two identical activities in the course, then
the best solution is to add some 'hidden' HTML in the activity (eg, adding a 
name or id attibute to one of the HTML tags)
