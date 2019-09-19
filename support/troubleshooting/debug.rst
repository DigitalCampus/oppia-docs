Capturing Oppia app Debug Log Output
====================================

To help with fixing bugs, there may be some times when having access to the 
full app debug log from the phone can be very useful. The steps below describe 
how to capture the Oppia debug log output to assist with bug fixing:


#. Install adb on your laptop (see: https://www.howtogeek.com/125769/how-to-install-and-use-abd-the-android-debug-bridge-utility/)
#. Enable USB debugging on your phone/device (under Settings > System > Developer Options,  you may need to enable developer options first - see: https://android.tutorials.how/enable-developer-options/)
#. Connect your phone to the laptop
#. Open the Oppia app on your phone
#. On the command line on your laptop run one of the following commands (
   depending on which operating system your laptop has):
   
   * Ubuntu/Linux: ``adb logcat | tee ~/oppia-output.txt``
   * Windows: ``adb logcat >> C:\oppia-output.txt``

#. Go through the steps/process to recreate the error on your phone. 
#. After you have caused the error, you can press Ctrl+C to stop the debug log 
   capturing.


.. note::
   If the developer options have been enabled on a users phone/device, it would 
   be best to disable the developer options after the log output has been saved 
   (again, see: https://android.tutorials.how/enable-developer-options/)
