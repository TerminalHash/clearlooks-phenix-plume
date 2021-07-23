## Overview

The Clearlooks-Phénix project aims at creating a GTK3 port of Clearlooks, the default theme for Gnome 2. Style is also included for GTK2, Unity and for Metacity, Openbox and Xfwm4 window managers.

This repo contains modified version of original port with purple colors (named Plume) from Tango Desktop Project, tweaked by me (TerminalHash). All copyrights to original authors.

### What i changed:

- Cinnamon theme - added, changed colors. // hidden

- GNOME Shell theme - added, changed colors. // hidden

- GTK3 theme - changed colors, description and name of theme, fixed bugs from theme parser.

- GTK2 theme - changed colors.

- Openbox theme - changed colors.

- Metacity theme - changed colors, description and other.

- Fluxbox theme - added, changed colors of pixmaps.

- PekWM theme - added, changed colors of pixmaps.

- IceWM theme - added, changed colors of pixmaps.

- XFWM4 theme - changed colors of pixmaps.

- qt5ct color scheme - added.

- TDE color scheme - added.

### Known bugs, errors, other

- Fluxbox and other WM themes untested and maybe extremely bugged!

- XFWM4 theme painted crookedly - I'm not very good at pixel art, so I tried my best.

- WM themes may not match in color  - everything is repainted by means of filters in GIMP.

- Shell and Cinnamon themes are experimental and not tested!

## Requirements


- Arch/Manjaro/Artix:

        pacman -S gtk-engines
        
- Alt Linux:

        apt-get install gtk2-engines
        
- APT/DEB based distros:

        apt install gtk2-engines OR apt-get install gtk2-engines

- OpenSUSE:

        zypper install gtk2-engines

- Fedora:

        dnf install gtk2-engines

- PCLinuxOS:

        apt-get install gtk-engines2

- ROSA Linux:

        urpmi gtk-engines2
        
- Mageia:

        urpmi gtk2-clearlooks-engine
        
- Solus:

        eopkg install gtk-engines
        
- Void:

        xbps-install -S gtk2-engines

## Installation

- Download archive from "Releases"

- Extract the archive.

- Rename the extracted folder to `Clearlooks-Phenix-Plume`.

- Copy the folder `Clearlooks-Phenix-Plume` in one of the following two locations:

	- `~/.themes/` for the current user;
	
	- `/usr/share/themes/` for all users, including style for programs ran with root privileges (e.g. Synaptic).

## Installation (WM Themes, color schemas)

- Fluxbox: copy directory "Clearlooks-Plume" to ~/.fluxbox/styles.

- IceWM: copy directory "IceClearlooks2-Plume" to ~/.icewm/themes.

- PekWM: copy directory "Clearlooks-Plume" to ~/.pekwm/themes.

- Qt5Ct: copy "Plume.conf" to ~/.config/qt5ct/colors.

- TDE: import file "TDE Plume.kcsrc" from Colors category.

### Selection

The theme must be selected once the installation is complete:

- On Gnome: with [gnome-tweak-tool](https://live.gnome.org/GnomeTweakTool), by setting *Theme > Window theme* and *Theme > GTK+ theme*, or in a terminal:

		dconf write /org/gnome/desktop/wm/preferences/theme \'Clearlooks-Phenix-Plume\'
		dconf write /org/gnome/desktop/interface/gtk-theme \'Clearlooks-Phenix-Plume\'

- On Xfce: by going to *Settings > Appearence > Style* in the main menu for the GTK theme, and to *Settings > Window Manager > Style* for the Xfwm4 theme, or in a terminal:

		xfconf-query -s Clearlooks-Phenix-Plume -c xfwm4 -p /general/theme
		xfconf-query -s Clearlooks-Phenix-Plume -c xsettings -p /Net/ThemeName
		
### Icon theme, yeah?

Use Mist, GNOME Noble (from GNOME Colors) or Tango icon themes.

I recommend you to use a Gnome Noble for match colors.

## Configuration

### Desktop managed by Nautilus

By default, the font color on a desktop managed by Nautilus is black. To set it to white, open the file `gtk-3.0/applications.css` with a text editor, find the code relative to Nautilus:

	/************
	 * Nautilus *
	 ************/
	
	/*
	COMMENTED
	CSS
	CODE
	*/

and uncomment it, as follows:

	/************
	 * Nautilus *
	 ************/
	
	UNCOMMENTED
	CSS
	CODE

To get a custom color, change the color directly in the file `gtk-3.0/applications.css`.

### Window buttons layout

If after installing or updating Ubuntu, the window buttons are on the left side, but you want them to the right, run the following command in a terminal:

	gconftool-2 --set /apps/metacity/general/button_layout --type string ":minimize,maximize,close"

### Wallpaper

The wallpaper used for the Gnome 3 desktop screenshot is available in the folder `wallpapers`.

## Development and license

[Original theme repository](https://github.com/jpfleury/clearlooks-phenix).

[Repository of this modification](https://github.com/TerminalHash/clearlooks-phenix-plume).

Thanks to Andrew Shadura and Andrey Cherepanov for the support of GTK 3.20, and to Yuri Khan for the support of HiDPI.

Author: Jean-Philippe Fleury (<http://www.jpfleury.net/en/contact.php>)  
Copyright © 2011-2014 Jean-Philippe Fleury  
Copyright © 2013-2014 Andrew Shadura
Copyright © 2021-2021 Leon Lisov

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.

### Third-party code

- Adwaita theme, from the package [`gnome-themes-standard`](http://packages.ubuntu.com/search?keywords=gnome-themes-standard), under LGPL.

- File `gtk-2.0/gtkrc`, from the package [`gtk2-engines`](http://packages.ubuntu.com/search?keywords=gtk2-engines), under LGPL.

- File `metacity-1/metacity-theme-1.xml`, from the package [`gnome-themes-selected`](http://packages.ubuntu.com/search?keywords=gnome-themes-selected), under LGPL.

- File `openbox-3/themerc`, from the package [`openbox`](http://packages.ubuntu.com/search?keywords=openbox), under GPL.

- [Clearlooks XFWM4](http://xfce-look.org/content/show.php/Clearlooks+for+XFWM4?content=137055) theme, under GPL.

- Files in `wallpapers`, based on an [image from volvoguy](http://gnome-look.org/content/show.php?content=22210), under GPL.

### Third-party files, added by TerminalHash

- IceWM theme from "Box Look" by ren-cs [IceClearlooks2 Color Mas Theme Pack](https://www.box-look.org/p/1310273/).

- "Plume" color scheme for Qt5Ct based on default scheme "Simple".

- Fluxbox theme by GotF [Clearlooks Fluxbox style](https://www.box-look.org/p/1017005/).

- PekWM theme by ?? [Beerlooks](https://www.box-look.org/p/1353095/).

- TDE color scheme "TDE Plume" based on default color scheme.

- Files from [TraditionalOK Clearlooks Colors](https://www.mate-look.org/p/1407000/) by rosaastrum:

		- mate-applications.css

		- other-applications.css

- GNOME Shell theme & Cinnamon theme picked from [Ambiance Crunchy](https://www.cinnamon-look.org/p/1013654/) by frombenny. // hidden
