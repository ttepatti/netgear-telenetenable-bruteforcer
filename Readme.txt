telnetenable.py by Paul Gebheim
Modified to work with newer Netgear routers (R7000, R7500) by insanid
Translated from the C source available from
http://wiki.openwrt.org/toh/netgear/telnet.console


Running:
python telnetenable.py <IP> <MAC> <Username> <Password>

IP - The IP of your Netgear device, usually 192.168.1.1

MAC - The mac address should be the MAC address of the LAN port on your Netgear device, WITHOUT the ":". e.g. "00:40:5E:21:14:4E" would be written as "00405E21144E".

For newer Netgear routers:
Username - 'admin'
Password = Use password you set in web interface

For older Netgear routers:
Username - Username for accessing the telnet console, usually 'Gearguy'
Password - Password for accessing the telnet console, usually 'Geardog'

Example usage:
python telnetenable.py 192.168.1.1 00405E21144E admin password
or
python telnetenable.py 192.168.1.1 00405E21144E Gearguy Geardog
