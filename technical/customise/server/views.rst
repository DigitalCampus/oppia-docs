Creating new database views
===============================

You can create database views to help hide some of the data structure
complexity if there are people who need to access the database directly to
extract data/reports for areas that aren't covered by the default dashboard
reports.

These views can be managed using the Django database migrations, to ensure they
are added to each implementation/instance of the database. OppiaMobile uses the 
`django-database-view <https://pypi.org/project/django-database-view/>`_ library
to assist with setting up and managing views.

Create new views
------------------

#. Under reports/models create new db view file
#. Run ``python manage.py makemigrations``
#. Then edit migration file:

   *  Add import ``from dbview.helpers import CreateView``
   *  Replace ``migrations.CreateModel`` with ``CreateView``
   *  Check the migration dependencies, you may need to add extra dependencies
      if you are referencing other models in your view
   
#. Now run ``python manage.py migrate``

During development and testing you might need to re-run this process several
times, eg, as you add columns etc to the output. In which case, each time you
edit the definition of you view you'll need to:

#. Delete the auto-generated (and edited) migration file
#. Drop the view from your database
#. Delete the row in the ``django_migrations`` table that references the
   migration has been applied 

Editing existing views
------------------------

need to be dropped then rebuilt?