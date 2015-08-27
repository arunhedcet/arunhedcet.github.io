---
layout: post
comments: true
title: How to fix double icons issue in plank/docky for google chrome and terminator
---

docky/plank double icon issue
=========================

You might have come across this issue while using docky/plank. You try open an application clicking on the icon in plank and out of nowhere another icon which looks different appears as the running app's icon. I've noticed this issue with two of my favorite apps terminator and google chrome.

I encountered the above mentioned issue when I tried to set terminator as my default terminal. When we start terminator it starts another executable called x-terminal-emulator so plank/docky cannot identify them as the same application. To correct this issue use this command

    sudo mv /usr/share/applications/terminator.desktop /usr/share/applications/x-terminal-emulator.desktop

The desktop file corresponding to terminator should be renamed to x-terminal-emulator.desktop. Remove the terminator icon from plank and add again from unity dash. This time x-terminal-emulator is getting added instead of terminator. Now if you open terminator you'll not see another icon corresponding to terminator.

The same issue can be seen with google chrome browser. To solve this you should rename the google-chrome.desktop file into google-chrome-stable.desktop.

    sudo mv /usr/share/applications/terminator.desktop /usr/share/applications/x    -terminal-emulator.desktop

Remove the chrome icon and add it from unity dash. You can use the same workaround for other applications also. Just find out if any other executable is running when you run the application.


