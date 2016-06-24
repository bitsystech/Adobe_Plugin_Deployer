# Deployment Guide
This project will help you install a plugin for any Adobe Creative Cloud application

---------------------------------------------------------------------------------------

If you want to build from scratch, use the following instructions:

1. You need to package this all inside /tmp/ so create a folder in your Package creation tool.
2. Something like /tmp/C3/ and keep the Contents folder here. 
3. Modify the script to execute the correct binary.
4. Keep the Apple script in the same temp folder.
5. Keep postinstall.sh as post install script to execute all the binaries and scripts.
6. Create a package using any utility.
7. Deploy and Test.


How it works:

1. The Bash Script calls the Apple script to kill application. (Yeah I know you can do this with bash as well)
2. Once InDesign is detected and killed, bash script continues and to install the plugin.
3. After Plugin installation, a notification is displayed using Cocoa Dialog.
4. If you want to make it better, you can use Cocoa Dialog to send out notification once installation is complete.
5. If you dont know what is Cocoa Dialog, then delete line #20-22 and if you know then correct the path in the script that is in line #8.  :)
