# SpyderApp_mac
Creating spyder app for opening spyder(installed without Anaconda) on macos

#### Step one
Install Spyder<br>
<b>pip install pyqt5<br>
pip install python-language-server</b><br>
download spyder repo from git<br>
unzip it and open terminal in spyder repo<br>
<b>sudo python setup.py install<b><br>
if spyder not opening add its path to PATH

#### Step Two
creating app<br>
download appify<br>
Give executable permission to the appify<br>
<b>chmod +x appify</b><br>
<b>which spyder</b><br>
copy the address displayed in terminal<br>
<b>touch script.sh</b><br>
<b>#!/bin/bash<br>spyder_address &<br>exit</b><br>
replace the spyder_address from the address copied from terminal<br>
<b>./appify script.sh "Spyder"</b><br>
Spyder.app is created

#### Step three
following instruction are valid for mac only<br>
open the pakage contents of app<br>
create a info.plist file under content folder<br>
Edit the info.plist<br>
<b>\<?xml version="1.0" encoding="UTF-8"?\><br>
\<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd" \><br>
\<plist version="1.0"\><br>
    \<dict\><br>
        \<key\>NSHighResolutionCapable\</key\><br>
        \<true /\><br>
        \<key\>CFBundleName\</key\><br>
        \<string\>Spyder\</string\><br>
    \</dict\><br>
\</plist\></b><br>
for changes to take effect<br>
<b>touch ./spyder.app</b><br>
open spyder.app info and change icon file<br>
###Spyder.app is Ready<br>
move the Spyder.app to application folder<br><br>
