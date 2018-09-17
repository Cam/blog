# How to fix connection issues in Safari on OSx Yosemite | Cam

##### 17th Mar, 2015 by [Cam][1]

Connecting to networks and websites can be amazingly "funky" (read "really unstable and annoying") in Apple's OSx Yosemite. There are problems with both WiFi and DNS.

To make matters worse, it is almost impossible to troubleshoot the issues, and the various "solutions" out there are generally only reported as successful by a small percentage of the people seeing the issues.

With that in mind, I am going to list some possible solutions below. These should be tried in order. If you have; anything to add, changes to recommend or success with any of these: please comment below.

## Basic Safari Maintenance

This should be your first stop in this adventure. These steps will fix a lot of otherwise undiagnosable issues.

1. Go to the Safari menu bar and click: Safari > Preferences > Privacy tab
2. Click "Remove All Website Data" and confirm
3. Open a Finder window
4. Go to the Finder menu bar and click: Go > Go to Folder
5. Paste the following into the text field
**~/Library/Caches/com.apple.Safari/Cache.db**
6. Click "Go"
7. Move the Cache.db file to the trash
8. Quit and relaunch Safari

## Troubleshoot Safari Extensions

This is something that you should do from time to time anyway, just to be sure none of your extensions are causing trouble.

1. Go to the Safari menu bar and click: Safari > Preferences > Extensions tab
2. Turn extensions "OFF" using the toggle at the top right
3. Quit and relaunch Safari

Did that help? If yes, one of your extensions is messing things up. Time to test each one...

1. Go back to the Extensions tab and toggle that switch back to "ON"
2. Un-tick "Enable ____" for every extension you have installed
3. Turn on ONE extension (generally start with your most used extensions)
4. Relaunch Safari

Did that help? If yes, you should uninstall the extension causing the problem. Continue this process with each extension you have installed.

## Use an alternative DNS provider

Apple themselves have recommended trying this. What we will do here is set up some popular DNS servers in our network settings. The 2 providers recommended by most are provided by Google and OpenDNS. Personally I prefer Google DNS.

### Google's DNS option

1. Open System Preferences, then go to Network > Advanced > DNS
2. Click "+"
3. Enter "**8.8.8.8**"
4. Click "+" again
5. Enter "**8.8.4.4**"

The steps are the same for OpenDNS, but the IP addresses to add are "**208.67.222.222**" and "**208.67.220.220**".

## Remove OSx's Network Configuration Files

1. Turn off your WiFi connectionPress enter a
2. Go to the Finder menu bar and click: Go > Go to Folder
3. Paste the following into the text field: **/Library/Preferences/SystemConfiguration/**
4. Click "Go"
5. Back up the following files to a folder somewhere on your computer (most choose the desktop for this)
    * _com.apple.airport.preferences.plist_
    * _com.apple.network.identification.plist_
    * _com.apple.wifi.message-tracer.plist _
    * _NetworkInterfaces.plist _
    * _preferences.plist_
6. Reboot your Mac
7. Turn on WiFi

I would recommend keeping a copy of those files for a little while in case something goes wrong. If you run into more problems, restore the files to their original location (i.e. /Library/Preferences/SystemConfiguration/).

## Restart the 'discoveryd' Service

1. Go to Application > Utilities
2. Open the "Terminal" app
3. Paste the following using "CMD+V"
**sudo launchctl unload -w /System/Library/LaunchDaemons/com.apple.discoveryd.plist**
4. Press "Enter" on your keyboard
5. Type your password and press "Enter" again
6. Paste the following, again using "CMD+V"
**sudo launchctl load -w /System/Library/LaunchDaemons/com.apple.discoveryd.plist**
7. Press "Enter" one more time
8. Restart any apps having trouble connecting (e.g. Safari)

## More possible solutions coming soon

I have a few more options available, and will add them when I have more time. The above options should be tried first in any case. Apparently some people have found that using a 2.4 GHz WiFi network rather than a 5GHz one fixes the problem. Switching off Bluetooth supposedly helps too.

These suggestions come from a number of different Apple support threads and [this post][2] on OSx Daily.

Any suggestions or feedback?

[1]: https://plus.google.com/+CamGould?rel=author
[2]: http://osxdaily.com/2014/10/25/fix-wi-fi-problems-os-x-yosemite/
