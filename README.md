This write-up is intended to quickly demonstrate how to install BlueZ on a Debian based system. It is not an introduction to Bluetooth or Bluetooth Low Energy (BLE). Raspberry Pi hardware was used to create a BLE based peripheral device, and the code is largely based on the gatt-server reference code included with BlueZ and a blog post from the company PunchThrough.

# BlueZ
BlueZ is the official Linux Bluetooth protocol that handles both Bluetooth BR/EDR (Classic) and BLE. It supports a variety of core Bluetooth features, layers, and protocols:
* Bluetooth kernel subsystem core
* L2CAP and SCO audio kernel layers
* RFCOMM, BNEP, CMTP and HIDP kernel implementations
* HCI UART, USB, PCMCIA and virtual device drivers
* General Bluetooth and SDP libraries and daemons
* Configuration and testing utilities
* Protocol decoding and analysis tools

#
# Installation From Source
OS Environment Tested:
```
pi@rpi4b-01:~ $ sudo cat /proc/device-tree/model       
Raspberry Pi 4 Model B Rev 1.1
pi@rpi4b-01:~ $ lsb_release -a
No LSB modules are available.
Distributor ID:	Raspbian
Description:	Raspbian GNU/Linux 10 (buster)
Release:	10
Codename:	buster
pi@rpi4b-01:~ $ uname -a
Linux rpi4b-01 5.10.17-v7l+ #1414 SMP Fri Apr 30 13:20:47 BST 2021 armv7l GNU/Linux
```
Required software packages:
```
Gcc compiler
GLib library
D-Bus library
udev library (optional)
readline (command line clients)
```
On debian based systems, this can be done by running the following command:
Enable debian source code by uncommenting deb-src in /etc/apt/sources.list and update source.list
```
sudo apt-get update
sudo apt-get build-dep bluez
```
To configure run:
```
./configure
```
To compile and install run:
```make
sudo make install
```
