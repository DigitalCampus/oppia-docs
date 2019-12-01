Configuring your own version of the server
===========================================

Additional Profile/Registration Fields
-----------------------------------------

You can add additional fields to the registration and profile forms by adding
entries in the Django Admin ``profile.CustomField`` table.

However you will also need to update the registration form in your app to make
sure the fields on this app form match those you have added on the server side.

.. note::
	If you set a CustomField to be required, before the app registration form
	has been updated and deployed, you will find that users will be unable to
	register an account. An approach to avoid this issue is to allow the new 
	CusomtField to be optional, until your app has been updated and deployed.

Overriding SCSS styles
----------------------

The CSS stylesheet of Oppia is generated using SASS, so to change the look and feel of the server, the best approach
is to modify the files under ``static/css``. If you are keen on SCSS, you can jump to the source
code and explore the different SCSS components for yourself.

The styles are an extension of `Daemonite's Material UI <http://daemonite.github.io/material/>`_ , modifying
Material default colors and adding some custom components.

For the basic customization of colors, you can edit the ``static/css/oppia.scss`` file. There you can edit
the Oppia defined colors and the different color palettes.

Compiling CSS custom styles
***************************

If you are in debug mode, the ``django-sass-processor`` will automatically re-compile the files that change,
but for a production environment, you'll need to precompile your SCSS files. For doing so, invoke first in the
command line the following parameter (with the virtual environment activated):

    ./manage.py compilescss

After that, you need to collect again the static files to update the ones in your public static folder:

    ./manage.py collectstatic --ignore=*.scss

The ``--collectstatic`` parameter is not mandatory, but is useful if you don't want to expose the SASS/SCSS files
in the production environment.
