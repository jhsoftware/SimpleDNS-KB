---
category: 14
frontpage: false
comments: true
refs: 46
created-utc: 2019-01-01
modified-utc: 2026-06-02
---
# Error message "Could not start DNS service on &lt;ip-address&gt; port 53 UDP. Port is used by another application" or "Could not start DNS service (Error 10048)"

This error message means that some other software on your computer is using the DNS port (53).

It could be that you are using "Internet Connection Sharing", which "maps" DNS requests and uses the same port (53) as DNS servers.  
See [How do I use Simple DNS Plus with Internet Connection Sharing?](/kb/132/using-simple-dns-plus-with-internet-connection-sharing-ics)

Proxy servers often include a DNS proxy/mapping function which can cause this.  
See [How do I use Simple DNS Plus with a proxy server?](/kb/56/how-do-i-use-simple-dns-plus-with-a-proxy-server)

Other software like network monitors could also by occupying port 53.

To find out what software is using the DNS port, at a command prompt, type `NETSTAT -nabp UDP` to also see which application is using each UDP port.

