# dwm - dynamic window manager
dwm is an extremely fast, small, and dynamic window manager for X. This is the configuration used on my machine
based on [gruvbox](https://github.com/morhetz/gruvbox/).

## Screenshots
![Sample Image](https://i.imgur.com/DL3A7Zj.png)
Wallpaper by [jefferyodom](https://wallpapersafari.com/w/ESgNJ5)

## Requirements
 - In order to build dwm you need the Xlib header files. 
 - To be able to display fonts, you need to install [Awesome Font](https://archlinux.org/packages/extra/any/ttf-font-awesome/).
 - To be able to modify the status bar, make sure  [xcompmgr](https://wiki.archlinux.org/title/xcompmgr) is installed. 

## Installed Patches
 - bar-height-spacing
 - color-bar
 - useless-gap


## Installation
Edit config.mk to match your local setup (dwm is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install dwm (if
necessary as root):

```
make clean install
```

## Running dwm
Add the following line to your .xinitrc to start dwm using startx:

```
exec dwm
```

In order to connect dwm to a specific display, make sure that
the DISPLAY environment variable is set correctly, e.g.:

```
 DISPLAY=foo.bar:1 exec dwm
```

The status bar bash script is saved in `dwm-status-bar`. To install it to your machine, add this to your `.xinitrc`
```
[ -f "path to repo"/dwm-status-bar ] && . "path to repo "/dwm-status-bar
```

## Configuration
The configuration of dwm is done by creating a custom config.h and (re)compiling the source code.
