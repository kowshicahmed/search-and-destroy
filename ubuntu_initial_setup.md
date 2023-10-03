
# Click to minimize

## with preview:

    $ gsettings set org.gnome.shell.extensions.dash-to-dock click-action 'minimize-or-overview'

## without preview:
    $ gsettings set org.gnome.shell.extensions.dash-to-dock click-action 'minimize'

## revert:
    $ gsettings reset org.gnome.shell.extensions.dash-to-dock click-action


# Launcher button on top
    $ gsettings set org.gnome.shell.extensions.dash-to-dock show-apps-at-top true

# revert:
    $ gsettings set org.gnome.shell.extensions.dash-to-dock show-apps-at-top false

# basic utilities setup

## for gdb gcc etc:

    $ sudo apt install build-essential
### or:
    $ sudo apt install build-essential gdb gcc
    
# Resolution fix 
    xrandr
    cvt [res] [res]
    sudo xrandr --newmode "1920x1080_60.00"  173.00  1920 2048 2248 2576  1080 1083 1088 1120 -hsync +vsync
    sudo xrandr --addmode Virtual1 1920x1080_60.00

## ipad res:
    sudo xrandr --newmode "2360x1640_60.00"  328.50  2360 2536 2792 3224  1640 1643 1653 1700 -hsync +vsync
    sudo xrandr --addmode Virtual1 "2360x1640_60.00"

