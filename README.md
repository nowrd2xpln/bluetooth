# BlueZ
Bluetooth related content

# Installation From Source
OS Environment Tested:
pi@rpi4b-01:~ $ lsb_release -a
No LSB modules are available.
Distributor ID:	Raspbian
Description:	Raspbian GNU/Linux 10 (buster)
Release:	10
Codename:	buster
pi@rpi4b-01:~ $ uname -a
Linux rpi4b-01 5.10.17-v7l+ #1414 SMP Fri Apr 30 13:20:47 BST 2021 armv7l GNU/Linux

Required software packages:
Gcc compiler
GLib library
D-Bus library
udev library (optional)
readline (command line clients)

On debian based systems, this can be done by running the following command:
Enable debian source code by uncommenting deb-src in /etc/apt/sources.list and update source.list
sudo apt-get update
sudo apt-get build-dep bluez

To configure run:
./configure

To compile and install run:
make
sudo make install
