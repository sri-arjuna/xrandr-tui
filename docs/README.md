README
======

This is a wrapper/wizard around xrandr.

If you are a laptop user, actualy use your laptop outside as well, 
and have an external monitor at home/office but wish it could be more simple?

This is a script that is thought for laptops, to assign for the monitor-toggle (fn+f4).

Also, it may help with other tasks around xrandr as updates will be applied.

This readme is not complete yet



Dependencies
------------
*	BASH
*	[xorg-xrandr ](http://www.x.org/wiki/Projects/XRandR/) (your distro should provide a package named likde this)
*	[TUI](https://savannah.nongnu.org/projects/tui/)


Install
-------

Simply put **xrandr-tui** in a BINDIR of your choice and install TUI manually, 
or use the **./configure** script to install xrandr-tui.

	su
	cd /usr/src
	git clone https://savannah.nongnu.org/projects/xrandr-tui
	cd xrandr-tui
	./configure --prefix=/usr
	make
	make install


Uninstall
-------

	su
	cd /usr/src/xrandr-tui
	make uninstall
	

Examples:
---------

Configure **xrandr-tui** by:

Well, connect your monitor to your laptop, and type:

	xrandr-tui --config

Also you can set your main output and its resolution, 
and if/when everything is messed up, simply call:

	xrandr-tui --reset


Within that configuration screen, you set your fallback output (_--reset_),
for laptop users this is usualy eDP1, for desktop users this may vary.

Once this one time setup is done, for any further action, simply call:

	xrandr-tui --switch
	
This should switch the display, deactivating the laptop screen, 
and showing the desktop on the external monitor.

When invoked again, this will be turned back.

Be aware, that the option-flags are automated,
for a more custom experience you should call xrandr-tui without options or arguments.
