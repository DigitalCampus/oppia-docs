Hosting Course and Media files on external service
=====================================================

Hosting the course and media files outside the Oppia server can improve performance when a lot of users are downloading
courses/media at the same time.


Configuration for external media/course hosting on AWS S3
-------------------------------------------------------------

On AWS S3
~~~~~~~~~~~~~~

#. Create a public bucket on S3 (eg 'my-oppia-bucket')
#. Create IAM user and give the user access to the bucket. Download/copy the ACCESS_KEY_ID and SECRET_ACCESS_KEY as you
   will need these when configuring the Oppia server
#. Update the bucket policy in the permission section::

    {
      "Version": "2012-10-17",
      "Statement": [
        {
          "Effect": "Allow",
          "Principal": "*",
          "Action": [
            "s3:GetObject"
          ],
          "Resource": "arn:aws:s3:::YOUR_BUCKET_NAME/*"
        }
      ]
    }

#. Update the Cross-origin resource sharing (CORS) options::

    [
      {
          "AllowedHeaders": [
              "Authorization",
              "Content-Length"
          ],
          "AllowedMethods": [
              "GET"
          ],
          "AllowedOrigins": [
              "*"
          ],
          "ExposeHeaders": [],
          "MaxAgeSeconds": 3000
      }
    ]

#. You can add a test file to your bucket and double check that the file is accessible publicly by downloading from a
   link in your browser.

Reference source for this setup and configuration: https://bobbyhadz.com/blog/aws-s3-allow-public-read-access


On Oppia server
~~~~~~~~~~~~~~~~~~~~~
#. Install s3fs: ``sudo apt install s3fs``
#. Store the IAM user information::

    echo ACCESS_KEY_ID:SECRET_ACCESS_KEY > /etc/passwd-s3fs

   and set the correct permissions for this file::

    chmod 600 /etc/passwd-s3fs

#. Create a directory for the bucket mounting::

    mkdir /home/oppia/s3

#. Mount the bucket as a local directory::

    /usr/bin/s3fs -o allow_other YOUR_BUCKET_NAME /home/oppia/s3/

#. For mounting after reboot, add the following to /etc/fstab::

    s3fs#YOUR_BUCKET_NAME /home/oppia/s3 fuse _netdev,allow_other,umask=227,uid=33,gid=33,use_cache=/root/cache 0 0

#. Reboot your Oppia server and check that the mounting is working correctly

#. In your Django ``settings_secret.py`` add::

    OPPIA_EXTERNAL_STORAGE = True

    OPPIA_EXTERNAL_STORAGE_MEDIA_ROOT = '/home/oppia/s3/media/'
    OPPIA_EXTERNAL_STORAGE_MEDIA_URL = 'https://<YOUR_BUCKET_NAME>.s3.<YOUR-AWS-REGION>.amazonaws.com/media/'

    OPPIA_EXTERNAL_STORAGE_COURSE_ROOT = '/home/oppia/s3/courses/'
    OPPIA_EXTERNAL_STORAGE_COURSE_URL = 'https://<YOUR_BUCKET_NAME>.s3.<YOUR-AWS-REGION>.amazonaws.com/courses/'

#. In the apache conf file for the site, remove::

    Alias /media /home/oppia/media/
    <Directory "/home/oppia/media/">
            Options MultiViews FollowSymLinks
            AllowOverride None
            Require all granted
    </Directory>

   and restart apache

#. If you are setting this up for an existing Oppia server with courses and media already uploaded, you should run the
   management command ``external_storage_sync``.

Reference source for locally mounting S3 bucket: https://www.howtogeek.com/devops/how-to-mount-an-s3-bucket-locally-on-linux/