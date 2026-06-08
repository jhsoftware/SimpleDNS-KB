---
category: 3
frontpage: false
comments: true
created-utc: 2019-01-01
modified-utc: 2019-01-01
---
# How do I update my domain name to be served by my own DNS servers?

You need to contact your registrar (the company you registered your domain name with) and have them change the DNS servers associated with your domain name (host records). Many registrars let you do this through a web-interface.

Typically, you would use names such as "ns1.your-domain-name.com" and "ns2..." pointing to the IP addresses of your own DNS servers.

Sometimes, it is necessary to create these "host records" (ns1... = IP address) before modifying your domain name settings.  
For example, if you registered your domain name with Network Solutions, you need to log in to your account and use the "Manage Host Servers" function.  
If you registered through another registrar, they may have a similar form or process this through e-mail - contact them for their exact procedures.

