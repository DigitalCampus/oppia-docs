Updating Content using Oppia Export Block v1.1.1 and above
===========================================================

Starting with Oppia Export Block v1.1.1, you can now specify if the course is a
draft/testing version or a live version when you start the process of exporting
from the block.

If draft/test is selected the course shortname will automatically have "-draft"
appended to it and be pushed as a draft course to the Oppia server.

In this way, you're able to push an updated draft/test version of a course that
is already live to users, without overwriting the currently live version of the
course.

Once you are happy with all the updates, you can publish as a live course and
then it will update the live version on the Oppia server, and get pushed out to
users.