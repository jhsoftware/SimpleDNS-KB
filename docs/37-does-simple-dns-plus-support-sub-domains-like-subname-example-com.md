---
category: 5
frontpage: false
comments: true
created-utc: 2019-01-01
modified-utc: 2019-01-01
---
# Does Simple DNS Plus support subdomains (like subname.example.com)?

Yes - there are basically 3 ways to create a subdomain:

1) If it is a simple subdomain name that only requires a single host record such as "printer4.example.com" = 192.168.11.22, then you would create it as an A-record in the parent zone (example.com):  
Click the "Records" button, right-click the parent zone in the left pane, select "New host..." from the pop-up menu, and enter the subdomain name and IP address.

If you have multiple subdomains which are all hosted on the same web-servers, e-mail-servers etc., you can even use wildcard records ( *.example.com ).  
This way you don't have to update the DNS configuration each time you add a new subdomain.

2) If the subdomain has multiple records itself (mail, web, ftp, etc.), then you would create it as a separate zone:  
Click the "Records" button, select "New -&gt; Zone", select "Primary zone", click the "Next" button, and the subdomain name as the zone name, click the "Finish" button.

3) If you want to delegate the subdomain to another DNS server set (for example, if you have a really cool domain name and can sell subdomains of it), then in the parent zone add NS-records for the subdomain name pointing to the DNS servers handling it.  
And make sure to add matching A-records (glue records) if the NS-records point to DNS server names which are themselves within the subdomain.

