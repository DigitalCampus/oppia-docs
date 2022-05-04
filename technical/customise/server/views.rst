Creating new database views
===============================

Docs in progress...

Uses django-database-view: https://github.com/manuelnaranjo/django-database-view

Create new views
------------------

#. Under reports/models create new db view
#. run makemigrations
#. then edit migration file:

   *  migrations.CreateModel > CreateView
   *  add from dbview.helpers import CreateView
  
#. Now run migrate


Editing existing views
------------------------

need to be dropped then rebuilt?