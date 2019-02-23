# How To Fix Disabled Edit Option In Shutter in Ubuntu 18.04


However, as Ubuntu Handbook noticed, you can download the .DEB files directly from a PPA and install them manually. This works in Ubuntu 18.04 smoothly. Let’s do that one by one.

1. Download libgoocanvas-common package first.

libgoocanvas-common

2. Next, get libgoocanvas3 package and install it by double clicking on it.

libgoocanvas3

3. In the end, download and install libgoo-canvas-perl package.

libgoo-canvas-perl

Once you have installed all the required dependencies, restart shutter. You may have to use ```sudo killall shutter``` command to kill all the running instances of Shutter or just restart your system.

You’ll see the edit option has been enabled again now.


