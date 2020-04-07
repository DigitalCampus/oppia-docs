Testing OppiaMobile Server
=======================================

The Oppia server uses `Django's inbuilt unit testing framework 
<https://docs.djangoproject.com/en/2.2/topics/testing/overview//>`_ .

Run the tests on your Oppia server
-----------------------------------

#. Activate the virtual environment (eg: ``/home/oppia/$ source env/bin/activate``)
#. Run all the tests with ``python manage.py test`` 


Creating new tests
-------------------

If you are adding additional functionality to the Oppia server, you can add 
tests for this functionality using the standard Django unit testing framework.

All the unit tests can be found under: 
https://github.com/DigitalCampus/django-oppia/tree/master/tests
