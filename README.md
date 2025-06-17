# Overview

This script is based on the original 'telnetenable.py' by Paul Gebheim, **and is currently heavily WORK IN PROGRESS.** This specific branch was spurred by my laziness - to use traditional TelnetEnable tooling, you need to know the MAC address of the LAN interface of your NETGEAR device. I didn't have this on hand, and my device was across the room, which got me thinking: Couldn't you simply bruteforce every possible MAC address in quick succession? And thus, this modification was born.

The overall goals of this mini project are:
- Update the script to work with Python 3
- Add MAC address bruteforcing to the script

# Usage

Running:

```sh
python telnetenable.py <IP> <MAC> <Username> <Password>
```

- IP = The IP of your Netgear device, usually 192.168.1.1
- MAC = The MAC address should be the MAC address of the LAN port on your Netgear device, WITHOUT the ":". e.g. "00:40:5E:21:14:4E" would be written as "00405E21144E".

For newer Netgear routers:
- Username = 'admin'
- Password = Use password you set in web interface

For older Netgear routers:
- Username = Username for accessing the telnet console, usually 'Gearguy'
- Password = Password for accessing the telnet console, usually 'Geardog'

Example usage:
```sh
python telnetenable.py 192.168.1.1 00405E21144E admin password
```
or, on an older Netgear device:
```sh
python telnetenable.py 192.168.1.1 00405E21144E Gearguy Geardog
```

# History

This script is based on the original 'telnetenable.py' by Paul Gebheim - originally over on [Google Code](https://code.google.com/archive/p/netgear-telnetenable/) (RIP that website), and then [brought over to GitHub](https://github.com/insanid/netgear-telenetenable) by insanid.

## Changelog

- Modified to work with newer Netgear routers (R7000, R7500) by insanid
- Translated from the C source available from: http://wiki.openwrt.org/toh/netgear/telnet.console
