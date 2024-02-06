
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


## Updating package list
	sudo apt update
	sudo apt upgrade 
	sudo apt dist-upgrade
	sudo apt autoremove
	sudo apt-get update

## Install CMake (at least version 3.13), and GCC cross compiler for raspberry pi pico
	sudo apt install cmake gcc-arm-none-eabi libnewlib-arm-none-eabi libstdc++-arm-none-eabi-newlib

## Installing C and C++ compilers
	sudo apt install build-essential

## Installing git
	sudo apt-get install git git-extras

## Setting up git user name and email
	git config --global user.name "user_name"
	git config --global user.email "email"

## Installing java 21 (amazon coretto)
	sudo apt install curl
	wget -O - https://apt.corretto.aws/corretto.key | sudo gpg --dearmor -o /usr/share/keyrings/corretto-keyring.gpg && \
	echo "deb [signed-by=/usr/share/keyrings/corretto-keyring.gpg] https://apt.corretto.aws stable main" | sudo tee /etc/apt/sources.list.d/corretto.list
	sudo apt-get update
	sudo apt-get install -y java-21-amazon-corretto-jdk

## Installing Gradle
	sudo curl -s "https://get.sdkman.io" | bash
	bash /home/akash/.sdkman/bin/sdkman-init.sh
	sdk version
	sdk install gradle