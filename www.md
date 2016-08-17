# How to map a domain name to an IP address?

## Public IP

For those who got hosts with a public IP address, you can set the public IP address for your domain name directly on your domain name register website.

## Private IP

Mostly you are using Wi-Fi through a router, then you got a private IP address. Unlike the public IP address, you have to:

1. Check out you public IP address, which is you router's public IP.
  1. Google/Baidu `ip`.
  2. CLI: `curl icanhazip.com`.
2. Manually configure an IP address for your PC/Mac, e.g. 192.168.1.222.
3. Start your web service on a specific port, e.g. 80.
4. Set a virtual server forwarding rule on your router, including: IP address (192.168.1.222), port (80), protocol (ALL).
