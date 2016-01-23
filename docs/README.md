README
======

This is a wrapper/wizard around xrandr.

If you are a laptop user, actualy use your laptop outside as well, 
and have an external monitor at home/office but wish it could be more simple?

Configure **xrandr-tui** by:

Well, connect your monitor to your laptop, and type:

	xrandr-tui --config

Within that configuration screen, you set your fallback output (__--reset__),
for laptop users this is usualy eDP1, for desktop users this may vary.

Once this one time setup is done, for any further action, simply call:

	xrandr-tui --switch
	
This should switch the display, deactivating the laptop screen, 
and showing the desktop on the external monitor.

When invoked again, this will be turned back.

Also you can set your main output and its resolution, 
and if/when everything is messed up, simply call:

	xrandr-tui --reset



Dependencies
------------
*	BASH
*	[xorg-xrandr ](http://www.x.org/wiki/Projects/XRandR/) (your distro should provide a package named likde this)
*	[TUI](https://savannah.nongnu.org/projects/tui/)




This is a script that is thought for laptops, to assign for the monitor-toggle (fn+f4).

Also, it may help with other tasks around xrandr as updates will be applied.

This readme is not complete yet

Installation
------------

Simply put **xrandr-tui** in a BINDIR of your choice, 
or use the **./configure** script to install xrandr-tui.
