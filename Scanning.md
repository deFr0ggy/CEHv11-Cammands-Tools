# NMAP

```
-sn --> disable port scan

-PP --> Timestamp PING

-PM --> Address Masl PING

-PS --> TCP SYN PING

-PA --> TCP ACK PING

-PE --> ICMP ECHO

-PU --> UDP PING

-PR --> ARP PING

-ST --> TCP Connect/Full Scan

-sS --> TCP Stealth Scan/Half Open

-sX --> XMAS Scan

-sM --> TCP Maimon Scan

-sA --> TCP ACK Scan

-sU --> UDP Scan

-sN --> NULL Scan

-sI --> IDLE/IPID Scan

-sY --> SCTP INIT Scan

-sZ --> SCTP Cookie Echo Scan

-sV --> Version Scanning

-A --> Agressive Scan

--script --> Scripts

-sC --> Safe Scripts

-v --> Verbose

-vv --> Very Verbose

-T (1,2,3,4,5) --> Timing

-O --> OS Discovery

```


# HPING3

```
hping3 --scan 0-65535 -S <Target>

hping3 -1 --> ICMP Scan

hping3 -2 --> UDP Scan

hping3 -F (FIN SCAN) -P (PUSH FLAG) -U (URG FLAG) -c (PACKETS COUNT) -p (PORT)
```


# OS Discovery

TTL --> 64 --> Linux
TTL --> 128 --> Windows


# Unicorn Scan
```
 unicornscan <target> -Iv
 unicornscan <target>:1-65535 -Iv
```


# Firewall Evasion

```
-f --> fragments
-g <port> --> souce manipulation
-mtu 8 --> Maximum Transmission Units (Packet Chunks)
-D RND:10 --> Decoy Generating Random Non-Reserved IPs
--data 0xdeadbeef --> data minipulation
--data-string "Hello World!" --> string manipulation
--data-length 2 --> length manipulation
--randomize-hosts --> random hosts
--badsum --> Bogus Checksums
```