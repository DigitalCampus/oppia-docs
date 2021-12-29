Preloading Users
================================

In cases where you are prerregistering the students and some of them might not
have internet connection available to log in the first time, the app can be
distributed with some users preloaded, so a local offline login can be
performed. 

.. note::
	Be aware that preloading a big amount of users (1000+) can make some
	background processes of the app to run slower.

To do so, a CSV file named `oppia_accounts.csv` must be added to the root
`files` folder of the app, including any number of users you want to be
added. This CSV file must include a header line to declare the fields order.

The "Export users" functionality of the server creates a file with the needed
format, but it can also be created manually. The fields that can be defined
in this file are:

 * `username`: Required. If a user with this username already existed in the
 app, because a normal login was done, his information will get updated with
 the data included in the file (password included, so be careful!).
 * `password`: Required. The password must be set in plain text. Once the
 file is preloaded, the password will be saved encrypted in the local database.
 * `apikey`: Required. The API Key of the user to be able to make authenticated
 requests to the server. It can be obtained from the user profile, or using
 the "Export users" functionality.
 * `email`: Optional.
 * `first_name`: Optional. 
 * `last_name`: Optional. 

You must use this specific identifiers in the header line of the CSV. Any other
fields included will be ignored.

In the next start of the app, it will fetch this file and load the users in the
local database. A message will be shown afterwards indicating the number of
users preloaded, or if there was any error in the CSV format. The app will
remove the file after processing it, so it is not processed in the future, and
also to avoid exposing the plain passwords of the users included in the CSV
file. 
