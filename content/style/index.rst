.. _styles:

Using stylesheets and javascript in your course
================================================

The Moodle oppia export block comes by default with a stylesheet and javascript 
file that will be applied to any courses you export - so the stylesheet, 
javascript and related resources (images etc) will get exported to the course 
package too.

You can see examples of the ``default.css`` stylesheet and javascript at 
:ref:`styles-default`

Creating your own style
------------------------
To add a new style (or adapt the existing one), create an new css file in the 
<block>/styles directory, along with a new directory for the resources (see the 
current folder structure). 