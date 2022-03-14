# John The Ripper

> Hash-ID

> Hash-Identifier

### MD5
> john --format=raw-md5 1.txt --wordlist=/usr/share/wordlists/rockyou.txt

### SHA1
```
john --format=raw-sha1 2.txt --wordlist=/usr/share/wordlists/rockyou.txt
```

### SHA256
```
john --format=raw-sha256 3.txt --wordlist=/usr/share/wordlists/rockyou.txt 
```

### BCrypt

```
john --format=bcrypt 4.txt --wordlist=/usr/share/wordlists/rockyou.txt 
```

> John Formats can be checked by using the following command. 

```
john --list-formats
```