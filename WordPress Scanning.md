# WordPress Scanning
> https://wpvulns.com/

> API: Ca5WBkEbHBt4aaBsR53liSNYseXRiBEtjzc13XCWT10

#### Simple Scan
```
wpscan --url <url>
```

#### Simple API Scan

```
wpscan --url <url> --api-token <api-token>
```

#### Enumerating Users
```
wpscan --url <url> --enumerate u
```

### Enumerating Vulnerable Plugins

```
wpscan --url <url> --enumerate vp
```

### Enumerating Vulnerable Themes
```
wpscan --url <url> --enumerate vt
```

### Enumerating Timb Thumbs
```
wpscan --url <url> --enumerate vt
```

#### Combined Scanning

```
wpscan --url <url> --enumerate vpt
```

### Enumerating Backups

```
wpscan --url <url> --enumerate cb
```

### Enumerating DB Exports
```
wpscan --url <url> --enumerate dbe
```

### Login BruteForce
```
wpscan --url <url> -U <userNames> -P <userPass>
```

### HTTP-Auth BruteForce
```
wpscan --url <url> --http-uth username:password
```

### Detection Modes

#### 1. Agressive

```
wpscan --url <url> --detection-mode agressive
```

#### 2. Passive

```
wpscan --url <url> --detection-mode passive
```

#### 3.  Mixed

```
wpscan --url <url> --detection-mode mixed
```

### Plugin Versions Detection Modes

#### 1. Agressive

```
wpscan --url <url> --plugin-detection-mode agressive
```

#### 2. Passive

```
wpscan --url <url> --plugin-detection-mode passive
```

#### 3. Mixed

```
wpscan --url <url> --plugin-detection-mode mixed
```

### Stealthy Scanning

```
wpscan --url <url> --stealthy
```

### User Enumeration (ID Based)
```
wpscan --url <url> --enumerate u1-20
```

### Media Enumeration (ID Based)

```
wpscan --url <url> --enumerate m1-1000
```

### Password Attack Types
#### 1. WP-LOGIN

```
wpscan --url <url> --password-attack wp-login
```

#### 2. XMLRPC

```
wpscan --url <url> --password-attack xmlrpc
```

#### 3. XMLRPC-MULTICALL

```
wpscan --url <url> --password-attack xmlrpc-multicall
```

### Login URL (If Not Default)

```
wpscan --url <url> -U <userName> -P <userPass> --login-url /blank
```




