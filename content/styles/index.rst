.. _styles:

Using stylesheets and javascript in your course
================================================

The Moodle Oppia export block comes by default with a stylesheet and javascript 
file that will be applied to any courses you export - so the stylesheet, 
javascript and related resources (images etc) will get exported to the course 
package too.

The block uses SCSS to generate the CSS file, to allow modifications and provide
a user friendly way to extend the base theme. This all gets compiled in runtime
into a single CSS file that gets included in the course package. 


.. toctree::
   :maxdepth: 1
   
   default/index
   noorahealth/index

Creating your own style
------------------------

By default, the Moodle block gives you a base style to extend from. To add a new
basic theme where you just want to modify the colors to your brand, create a new
SCSS file in the ``<block>/styles/themes`` directory with the name of your
theme. In this SCSS file, you just need to define the color palette for your
theme (you can copy the ``default.scss`` to view the current definitions)::


	$primary-color: #77A240;
	$primary-color-dark: #597725;
	$secondary-color: #a5c727;
	$table-border-color: #111;
	$table-header-bg-color: $primary-color;

Then, you need to create a new directory for the style resources with the name
of ``{{your_theme_name}}-style-resources`` (see the current folder structure
for reference), that will get copied over to the course package.

If you new additional styles, you can create an additional SCSS file in the 
``<block>/styles/themes`` folder with the name 
``{{your_theme_name}}_extra.scss``. This file will get compiled in the final
CSS file as well, appending and overriding all the styles included to the base
stylesheet. You can also make use of the color variables defined in the other
theme file.
