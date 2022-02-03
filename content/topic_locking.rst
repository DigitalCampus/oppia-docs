Locking Topics with Password
=============================

As of :ref:`block version 1.3.0<blockv1.3.0>` and :ref:`app version 7.3.6<appv96>`
you can set a password for specific topics, so users in the app can only access
these topics once they have been given the password.

Password locking topics is not a native feature of Moodle, so setting which 
topics have a password is set up in the Moodle - Oppia export block in step 2. 
For any topics you don't want to have a password, just leave the password field
blank.

Once a password is set user will need to enter the correct password to access 
any of the activities in that topic, although they will still be able to see the 
activity titles and type from the course index page.

After a user has entered the correct password, they will only need to enter it 
once. Even if they log out and back in to the app, they won't need to enter the 
password again. However, if the course is updated and a new password is set, the 
topic will be 're-locked' and the user will need to enter the new password to 
access again. 

If another user logs into the same device, they will need to enter the password.

Activies within a still unlocked topic will not show in any search results.

