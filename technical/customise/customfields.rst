Adding extra registration form fields
=========================================

By default, OppiaMobile provides some basic user profile with some of the most common fields needed for an implementation. This includes first name, last name, email, or job title and organization the user belongs to. If there is a need to have some additional fields, there is a simple way to customize them.

The system allows the definition of three custom field types:
* **String** values: for any kind of text form
* **Integer** values, for numerical fields
* **Boolean** values, for yes/no conditions, or a simple "License agreement", for example.

Server
-------

The profile custom fields can be edited dynamically from the user interface, so there is no change in configuration files needed. 

This is done using the Django admin, so access it from the navigation bar (you have to be a user with admin rights) and go to the "Profile > Custom fields" section. There you can edit the current ones, remove them or add new fields.

.. image:: images/customfield-django.png
    :align: center

* The **Id** field is the dictionary identifier for that field. Name it using the `snake_case` style, so for example, if you want to add a "Twitter username" field, you would name it `twitter_profile`. 

* The **"helper text"** field is used to define a explanatory text for that field that will be displayed on the form below the input.

* The **order** value is used to control how the custom fields are ordered within the form.

Be careful with adding additional required fields for apps already deployed, since that could cause that a version of the app that doesn't include that field in the registration form would not be able to submit new users, as the form would not be validated because of that missing field.


App
----

Once the server is ready to manage the custom fields, we need to configure them in the app. Right now this is done in the building process, so there is no way of dynamically edit the form fields once the app has been built. In future versions of the app, the custom fields definition will be directly fetched from the server, but this process is needed anyway for a first definition and in cases where the app will work mostly offline.

The custom fields are defined in a file named `custom_fields.json` under the `assets` folder. You have to update this dictionary with the proper syntax. Here is an example of how that JSON would look like (reading the description of server custom fields the example itself is pretty much self-explanatory):

```
{
	"fields": [
		{
			"name":"custom_text",
			"label":"Required field",
			"order":1,
			"required":true,
			"helper_text":"....",
			"type":"str"
		},

		{
			"name":"custom_bool",
			"label":"Boolean field",
			"order":2,
			"required":false,
			"helper_text":"Check this to field",
			"type":"bool"
		},

		{
			"name":"custom_int",
			"label":"Numeric field",
			"order":3,
			"required":false,
			"helper_text":"....",
			"type":"int"
		}

		// ... 

	]
}
```	

The custom fields are loaded once per app version, so if you want to update the custom fields definition of a previously installed app, you'll have to update the `LOAD_CUSTOMFIELDS_VERSION` build setting (see :doc:`./settings`) to a higher value. If the value is the same of the current app version, you'll need to update also your app `versionCode` in Gradle for this changes to be reflected.

Note that the custom fields defined in the JSON will not add new fields defined but **override** the current definition with that one, so any field that is no longer there will be removed. This does not include the current values saved for the local users of the app, only the definition of what fields appear in the UI, so those values would be kept in the local database.
