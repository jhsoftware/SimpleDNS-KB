---
category: 1
frontpage: false
comments: true
created-utc: 2019-01-01
modified-utc: 2026-05-04
---
# Does the 10/20-connection limit on Desktop versions of Windows affect Simple DNS Plus?

The short answer is NO.

Desktop versions of Windows do limit simultaneous inbound **TCP connections** (license wise and/or technically).  
Specifically, Windows XP / Vista limits this to 10 connections, and Windows 7 / 8 / 8.1 / 10 / 11 limits it to 20 connections.

However, most DNS requests are not sent via TCP. They are sent via **UDP**, which is a connectionless protocol, and therefore cannot really be limited.

DNS generally only uses TCP connections for zone transfers. So this limitation would only be a problem if you have more than 10/20 secondary DNS servers all trying to connect at the same time.

