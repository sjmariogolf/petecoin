
Debian
====================
This directory contains files used to package petecoind/petecoin-qt
for Debian-based Linux systems. If you compile petecoind/petecoin-qt yourself, there are some useful files here.

## petecoin: URI support ##


petecoin-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install petecoin-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your petecoin-qt binary to `/usr/bin`
and the `../../share/pixmaps/petecoin128.png` to `/usr/share/pixmaps`

petecoin-qt.protocol (KDE)

