This script runs in the background on a 1 minute loop checking to see if I have a window open with the words 'Netflix', 'YouTube' or 'pdfpc' in the window title. If this condition is met, it will issue a 'xautolock -disable' so that xautolock doesn't boot me out of my session due to inactivity. This is useful on my system where xautolock doesn't seem to follow form with becoming inactive when partaking in activities where you won't be using the computer, but want the screen left on.

It also runs 'xautolock -enable' when there is no window with those strings in the title. I added a dontspam bit because if xautolock is sent the enable command once per minute, it keeps resetting the countdown clock aka: never locks the screen.

Finally it updates an icon in the AwesomeWM wibar so that you know if it's engaged or not. Meant to have a similar look to 'caffeine' from gnome3.


Invocation
---------------
You can call this script from your ~/.xinitrc or in my case ~/.config/awesome/rc.lua


Dependancies
---------------
You need the 'wmctrl' and 'xautolock' commands installed
