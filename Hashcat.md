# HashCat

> https://www.tunnelsup.com/hash-analyzer/

> CrachStation

> Hashkiller

### SHA 1

```
hashcat -m 100 1.txt /usr/share/wordlists/rockyou.txt
```

### SHA 256

```
hashcat -m 1400 1.txt /usr/share/wordlists/rockyou.txt
```

### BCrypt

```
hashcat -m 3200 1.txt /usr/share/wordlists/rockyou.txt 
```

### MD4

```
hashcat -m 900 1.txt /usr/share/wordlists/rockyou.txt
```

### NTLM

```
hashcat -m 1000 1.txt /usr/share/wordlists/rockyou.txt 
```