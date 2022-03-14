# Enumeration

### 1. NetBIOS
```
Command Line

nbtstat -a <IP> --> Windows
nbtstat -c --> Windows
net use --> Windows
nbtscan --> Linux


Softwares

NetBIOS Enumerator
ZENMAP
nmap -sC -sV -T4 -A --script=nbtstat.nse <IP>
nmap -sU -T4 -A --script=nbtstat.nse <IP>
```

#### 2. SNMP 
```
Command Line 

snmp-check
snmpcheck
snmpwalk

Softwares

SoftPerfect Network Scanner
```

#### 3. LDAP 

```
Active Directory Explorer
```

#### 4. NFS 

```
superEnum
RPCscan
NMAP to the Rescure
```

#### 5. DNS
```
dig ns <domain>
dig <ns1> <domain> axfr --> Zone Transfer
```

```
nslookup 

set querytype = soa, mx, ns, txt, a

<domain>

ls -d <name servers>
```

```
dnsrecon -d <domain> -z
```


#### 6. Linux/Windows Enumeration

```
enum4linux -u <username> -p <password> -n <Target>

enum4linux -u <username> -p <password> -U <target>

enum4linux -u <username> -p <password> -o <target>

enum4linux -u <username> -p <password> -P <target>

enum4linux -u <username> -p <password> -G <target>

enum4linux -u <username> -p <passwrod> -S <target>


```

> https://book.hacktricks.xyz/pentesting/