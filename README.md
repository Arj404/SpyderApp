# SpyderApp_mac
Creating spyder app for opening spyder(installed via pip) on macos


Give executable permission to the appify<b>chmod +x appify</b><br>
<b>which spyder</b><br>
copy the address displayed in terminal<br>
create a script file <b>touch script.sh</b><br>
edit the script<br>
<b>#!/bin/bash<br>spyder_address &<br>exit</b><br>
replace the spyder_address from the address copied from terminal<br>
<b>./appify script.sh "spyder"</b><br>
spyder.app is created<br>

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
for changes to take effect <b>touch ./spyder.app</b><br>
open spyder.app info and change icon file<br>
###Spyder.app is Ready
