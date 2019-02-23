# shutter_fix_edit
Fix Shutter in Ubuntu 18.04
You are here: Home / How To / How To Fix Disabled Edit Option In Shutter in Ubuntu 18.04 & Mint 19
How To Fix Disabled Edit Option In Shutter in Ubuntu 18.04 & Mint 19
Last updated September 2, 2018 By Abhishek Prakash 119 Comments

Brief: Found edit option disabled in Shutter? Don’t worry, here is the quick fix for it.

One of my favorite image editing tools in Linux is Shutter. Shutter is primarily a screenshot tool but it provides added advantage of quickly editing the screenshots, resizing and a lot other things related to images. Most of the tutorials on It’s FOSS have been edited on Shutter. If I may, I would call it Swiss Army knife of screenshots. One tool to rule them all. Clearly, it’s one of the best screenshot tools available for Linux.

For me, getting Shutter was one of the first few things to do after installing Ubuntu 18.04. But there is this little issue with Shutter that I noticed. The edit option in Shutter was disabled. Quite frustrating, I know.

Fixing disabled button in Shutter on Ubuntu 18.04
Not only that, the applet indicator on the top panel was also missing. In this quick tutorial, I’ll show you how to fix disabled edit option in Shutter and how to get the Shutter app indicator back as well.

Enable edit option in Shutter in Ubuntu 18.04 & Mint 19
The problem here is that Shutter application has not been updated in a long time. It is still using some programs and libraries underneath it that have been replaced by their newer versions in the recent Ubuntu releases.

Naturally, it still depends on the older libraries and cannot find it and thus the Edit option is not available to you.

The main developer for Shutter is missing in action for a couple of years and thus updating Shutter itself is a challenge. There are talks about releasing a Snap version of Shutter that will have all the dependencies. 

While the discussion is ongoing, you can manually install the dependencies as a workaround to enable the edit option in Shutter. But there is another problem here. These older libraries are no longer in Ubuntu’s repositories. So you cannot install them the standard way.

However, as Ubuntu Handbook noticed, you can download the .DEB files directly from a PPA and install them manually. This works in Ubuntu 18.04 smoothly. Let’s do that one by one.

1. Download libgoocanvas-common package first. Just double-click on the downloaded file to install it with Software Center. You can also use Gdebi or command line.

libgoocanvas-common

2. Next, get libgoocanvas3 package and install it by double clicking on it.

libgoocanvas3

3. In the end, download and install libgoo-canvas-perl package.

libgoo-canvas-perl

Once you have installed all the required dependencies, restart shutter. You may have to use sudo killall shutter command to kill all the running instances of Shutter or just restart your system.

You’ll see the edit option has been enabled again now.

Fix disabled edit option in Shutter
Get applet indicator for Shutter
You might even remember that Shutter has(d) an applet indicator. This app-indicator gave quick access to all the Shutter features from the top panel. If you want, you can get it back as well.

Use the commands below to enable Shutter app-indicator:

sudo apt install libappindicator-dev
And after that install a Perl module:

sudo cpan -i Gtk2::AppIndicator
Restart Shutter and you should see the applet indicator on the top panel in Ubuntu 18.04.

Enable edit option in Shutter on Ubuntu
