---
category: 11
frontpage: false
comments: true
created-utc: 2019-01-01
modified-utc: 2026-08-03
---
# Using Simple DNS Plus with Internet Connection Sharing (ICS)

Windows has a built-in "Internet Connection Sharing" (ICS) feature.  
This feature is a very simple NAT server, DNS proxy, and DHCP server (a.k.a. "DHCP allocation service") combination which makes it easy to share the Internet connection of one PC with other PCs on a local area network.

If you run Simple DNS Plus on the computer that shares the Internet connection, ICS may conflict with Simple DNS Plus because it uses the same TCP/IP ports.

ICS listens for DNS requests on the private side network connection (IP 192.168.0.1 port 53) and forwards these to the DNS server that the ICS computer is configured to use.  
And it listens for DHCP requests on the private side network connection (IP 192.168.0.1 port 67) and assigns clients IP addresses in the 192.168.0.xxx range.  
This is not configurable in any way.

If the computer sharing the Internet connection has two network cards with fixed IP addresses (one for the Internet and one for the local area network), configure Simple DNS Plus to listen on the Internet IP address only.  
Otherwise configure Simple DNS Plus to listen on 127.0.0.1 only.

In the Simple DNS Plus main window, click the "Options" button:

![](img/132/1.png)

Select "Inbound Requests" in the left list, select "On the IP addresses checked below", make sure only 127.0.0.1 or the Internet IP address is checked, and click the "OK" button to save your changes:

![](img/132/2.png)

