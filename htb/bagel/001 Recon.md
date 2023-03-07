
# Nmap 
```
Nmap scan report for 10.10.11.201
Host is up (0.069s latency).
Not shown: 997 closed tcp ports (reset)
PORT     STATE SERVICE  VERSION
22/tcp   open  ssh      OpenSSH 8.8 (protocol 2.0)
| ssh-hostkey: 
|   256 6e4e1341f2fed9e0f7275bededcc68c2 (ECDSA)
|_  256 80a7cd10e72fdb958b869b1b20652a98 (ED25519)
5000/tcp open  upnp?
| fingerprint-strings: 
|   GetRequest: 
|     HTTP/1.1 400 Bad Request
|     Server: Microsoft-NetCore/2.0
|     Date: Mon, 27 Feb 2023 22:18:39 GMT
|     Connection: close
|   HTTPOptions: 
|     HTTP/1.1 400 Bad Request
|     Server: Microsoft-NetCore/2.0
|     Date: Mon, 27 Feb 2023 22:18:54 GMT
|     Connection: close
|   Help, SSLSessionReq, TerminalServerCookie: 
|     HTTP/1.1 400 Bad Request
|     Content-Type: text/html
|     Server: Microsoft-NetCore/2.0
|     Date: Mon, 27 Feb 2023 22:19:05 GMT
|     Content-Length: 52
|     Connection: close
|     Keep-Alive: true
|     <h1>Bad Request (Invalid request line (parts).)</h1>
|   RTSPRequest: 
|     HTTP/1.1 400 Bad Request
|     Content-Type: text/html
|     Server: Microsoft-NetCore/2.0
|     Date: Mon, 27 Feb 2023 22:18:39 GMT
|     Content-Length: 54
|     Connection: close
|     Keep-Alive: true
|     <h1>Bad Request (Invalid request line (version).)</h1>
|   TLSSessionReq: 
|     HTTP/1.1 400 Bad Request
|     Content-Type: text/html
|     Server: Microsoft-NetCore/2.0
|     Date: Mon, 27 Feb 2023 22:19:06 GMT
|     Content-Length: 52
|     Connection: close
|     Keep-Alive: true
|_    <h1>Bad Request (Invalid request line (parts).)</h1>
8000/tcp open  http-alt Werkzeug/2.2.2 Python/3.10.9
| http-methods: 
|_  Supported Methods: HEAD OPTIONS GET
|_http-title: Did not follow redirect to http://bagel.htb:8000/?page=index.html
| fingerprint-strings: 
|   FourOhFourRequest: 
|     HTTP/1.1 404 NOT FOUND
|     Server: Werkzeug/2.2.2 Python/3.10.9
|     Date: Mon, 27 Feb 2023 22:18:39 GMT
|     Content-Type: text/html; charset=utf-8
|     Content-Length: 207
|     Connection: close
|     <!doctype html>
|     <html lang=en>
|     <title>404 Not Found</title>
|     <h1>Not Found</h1>
|     <p>The requested URL was not found on the server. If you entered the URL manually please check your spelling and try again.</p>
|   GetRequest: 
|     HTTP/1.1 302 FOUND
|     Server: Werkzeug/2.2.2 Python/3.10.9
|     Date: Mon, 27 Feb 2023 22:18:34 GMT
|     Content-Type: text/html; charset=utf-8
|     Content-Length: 263
|     Location: http://bagel.htb:8000/?page=index.html
|     Connection: close
|     <!doctype html>
|     <html lang=en>
|     <title>Redirecting...</title>
|     <h1>Redirecting...</h1>
|     <p>You should be redirected automatically to the target URL: <a href="http://bagel.htb:8000/?page=index.html">http://bagel.htb:8000/?page=index.html</a>. If not, click the link.
|   Socks5: 
|     <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
|     "http://www.w3.org/TR/html4/strict.dtd">
|     <html>
|     <head>
|     <meta http-equiv="Content-Type" content="text/html;charset=utf-8">
|     <title>Error response</title>
|     </head>
|     <body>
|     <h1>Error response</h1>
|     <p>Error code: 400</p>
|     <p>Message: Bad request syntax ('
|     ').</p>
|     <p>Error code explanation: HTTPStatus.BAD_REQUEST - Bad request syntax or unsupported method.</p>
|     </body>
|_    </html>
|_http-server-header: Werkzeug/2.2.2 Python/3.10.9
2 services unrecognized despite returning data. If you know the service/version, please submit the following fingerprints at https://nmap.org/cgi-bin/submit.cgi?new-service :
==============NEXT SERVICE FINGERPRINT (SUBMIT INDIVIDUALLY)==============
SF-Port5000-TCP:V=7.93%I=7%D=2/28%Time=63FD2C3A%P=x86_64-pc-linux-gnu%r(Ge
SF:tRequest,73,"HTTP/1\.1\x20400\x20Bad\x20Request\r\nServer:\x20Microsoft
SF:-NetCore/2\.0\r\nDate:\x20Mon,\x2027\x20Feb\x202023\x2022:18:39\x20GMT\
SF:r\nConnection:\x20close\r\n\r\n")%r(RTSPRequest,E8,"HTTP/1\.1\x20400\x2
SF:0Bad\x20Request\r\nContent-Type:\x20text/html\r\nServer:\x20Microsoft-N
SF:etCore/2\.0\r\nDate:\x20Mon,\x2027\x20Feb\x202023\x2022:18:39\x20GMT\r\
SF:nContent-Length:\x2054\r\nConnection:\x20close\r\nKeep-Alive:\x20true\r
SF:\n\r\n<h1>Bad\x20Request\x20\(Invalid\x20request\x20line\x20\(version\)
SF:\.\)</h1>")%r(HTTPOptions,73,"HTTP/1\.1\x20400\x20Bad\x20Request\r\nSer
SF:ver:\x20Microsoft-NetCore/2\.0\r\nDate:\x20Mon,\x2027\x20Feb\x202023\x2
SF:022:18:54\x20GMT\r\nConnection:\x20close\r\n\r\n")%r(Help,E6,"HTTP/1\.1
SF:\x20400\x20Bad\x20Request\r\nContent-Type:\x20text/html\r\nServer:\x20M
SF:icrosoft-NetCore/2\.0\r\nDate:\x20Mon,\x2027\x20Feb\x202023\x2022:19:05
SF:\x20GMT\r\nContent-Length:\x2052\r\nConnection:\x20close\r\nKeep-Alive:
SF:\x20true\r\n\r\n<h1>Bad\x20Request\x20\(Invalid\x20request\x20line\x20\
SF:(parts\)\.\)</h1>")%r(SSLSessionReq,E6,"HTTP/1\.1\x20400\x20Bad\x20Requ
SF:est\r\nContent-Type:\x20text/html\r\nServer:\x20Microsoft-NetCore/2\.0\
SF:r\nDate:\x20Mon,\x2027\x20Feb\x202023\x2022:19:05\x20GMT\r\nContent-Len
SF:gth:\x2052\r\nConnection:\x20close\r\nKeep-Alive:\x20true\r\n\r\n<h1>Ba
SF:d\x20Request\x20\(Invalid\x20request\x20line\x20\(parts\)\.\)</h1>")%r(
SF:TerminalServerCookie,E6,"HTTP/1\.1\x20400\x20Bad\x20Request\r\nContent-
SF:Type:\x20text/html\r\nServer:\x20Microsoft-NetCore/2\.0\r\nDate:\x20Mon
SF:,\x2027\x20Feb\x202023\x2022:19:05\x20GMT\r\nContent-Length:\x2052\r\nC
SF:onnection:\x20close\r\nKeep-Alive:\x20true\r\n\r\n<h1>Bad\x20Request\x2
SF:0\(Invalid\x20request\x20line\x20\(parts\)\.\)</h1>")%r(TLSSessionReq,E
SF:6,"HTTP/1\.1\x20400\x20Bad\x20Request\r\nContent-Type:\x20text/html\r\n
SF:Server:\x20Microsoft-NetCore/2\.0\r\nDate:\x20Mon,\x2027\x20Feb\x202023
SF:\x2022:19:06\x20GMT\r\nContent-Length:\x2052\r\nConnection:\x20close\r\
SF:nKeep-Alive:\x20true\r\n\r\n<h1>Bad\x20Request\x20\(Invalid\x20request\
SF:x20line\x20\(parts\)\.\)</h1>");
==============NEXT SERVICE FINGERPRINT (SUBMIT INDIVIDUALLY)==============
SF-Port8000-TCP:V=7.93%I=7%D=2/28%Time=63FD2C35%P=x86_64-pc-linux-gnu%r(Ge
SF:tRequest,1EA,"HTTP/1\.1\x20302\x20FOUND\r\nServer:\x20Werkzeug/2\.2\.2\
SF:x20Python/3\.10\.9\r\nDate:\x20Mon,\x2027\x20Feb\x202023\x2022:18:34\x2
SF:0GMT\r\nContent-Type:\x20text/html;\x20charset=utf-8\r\nContent-Length:
SF:\x20263\r\nLocation:\x20http://bagel\.htb:8000/\?page=index\.html\r\nCo
SF:nnection:\x20close\r\n\r\n<!doctype\x20html>\n<html\x20lang=en>\n<title
SF:>Redirecting\.\.\.</title>\n<h1>Redirecting\.\.\.</h1>\n<p>You\x20shoul
SF:d\x20be\x20redirected\x20automatically\x20to\x20the\x20target\x20URL:\x
SF:20<a\x20href=\"http://bagel\.htb:8000/\?page=index\.html\">http://bagel
SF:\.htb:8000/\?page=index\.html</a>\.\x20If\x20not,\x20click\x20the\x20li
SF:nk\.\n")%r(FourOhFourRequest,184,"HTTP/1\.1\x20404\x20NOT\x20FOUND\r\nS
SF:erver:\x20Werkzeug/2\.2\.2\x20Python/3\.10\.9\r\nDate:\x20Mon,\x2027\x2
SF:0Feb\x202023\x2022:18:39\x20GMT\r\nContent-Type:\x20text/html;\x20chars
SF:et=utf-8\r\nContent-Length:\x20207\r\nConnection:\x20close\r\n\r\n<!doc
SF:type\x20html>\n<html\x20lang=en>\n<title>404\x20Not\x20Found</title>\n<
SF:h1>Not\x20Found</h1>\n<p>The\x20requested\x20URL\x20was\x20not\x20found
SF:\x20on\x20the\x20server\.\x20If\x20you\x20entered\x20the\x20URL\x20manu
SF:ally\x20please\x20check\x20your\x20spelling\x20and\x20try\x20again\.</p
SF:>\n")%r(Socks5,213,"<!DOCTYPE\x20HTML\x20PUBLIC\x20\"-//W3C//DTD\x20HTM
SF:L\x204\.01//EN\"\n\x20\x20\x20\x20\x20\x20\x20\x20\"http://www\.w3\.org
SF:/TR/html4/strict\.dtd\">\n<html>\n\x20\x20\x20\x20<head>\n\x20\x20\x20\
SF:x20\x20\x20\x20\x20<meta\x20http-equiv=\"Content-Type\"\x20content=\"te
SF:xt/html;charset=utf-8\">\n\x20\x20\x20\x20\x20\x20\x20\x20<title>Error\
SF:x20response</title>\n\x20\x20\x20\x20</head>\n\x20\x20\x20\x20<body>\n\
SF:x20\x20\x20\x20\x20\x20\x20\x20<h1>Error\x20response</h1>\n\x20\x20\x20
SF:\x20\x20\x20\x20\x20<p>Error\x20code:\x20400</p>\n\x20\x20\x20\x20\x20\
SF:x20\x20\x20<p>Message:\x20Bad\x20request\x20syntax\x20\('\\x05\\x04\\x0
SF:0\\x01\\x02\\x80\\x05\\x01\\x00\\x03'\)\.</p>\n\x20\x20\x20\x20\x20\x20
SF:\x20\x20<p>Error\x20code\x20explanation:\x20HTTPStatus\.BAD_REQUEST\x20
SF:-\x20Bad\x20request\x20syntax\x20or\x20unsupported\x20method\.</p>\n\x2
SF:0\x20\x20\x20</body>\n</html>\n");

NSE: Script Post-scanning.
Initiating NSE at 08:20
Completed NSE at 08:20, 0.00s elapsed
Initiating NSE at 08:20
Completed NSE at 08:20, 0.00s elapsed
Initiating NSE at 08:20
Completed NSE at 08:20, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 106.25 seconds
           Raw packets sent: 1004 (44.152KB) | Rcvd: 1001 (40.040KB)
```


# Webpage

webpage has **?page=**
can get /etc/passwd
```
root:x:0:0:root:/root:/bin/bash
bin:x:1:1:bin:/bin:/sbin/nologin
daemon:x:2:2:daemon:/sbin:/sbin/nologin
adm:x:3:4:adm:/var/adm:/sbin/nologin
lp:x:4:7:lp:/var/spool/lpd:/sbin/nologin
sync:x:5:0:sync:/sbin:/bin/sync
shutdown:x:6:0:shutdown:/sbin:/sbin/shutdown
halt:x:7:0:halt:/sbin:/sbin/halt
mail:x:8:12:mail:/var/spool/mail:/sbin/nologin
operator:x:11:0:operator:/root:/sbin/nologin
games:x:12:100:games:/usr/games:/sbin/nologin
ftp:x:14:50:FTP User:/var/ftp:/sbin/nologin
nobody:x:65534:65534:Kernel Overflow User:/:/sbin/nologin
dbus:x:81:81:System message bus:/:/sbin/nologin
tss:x:59:59:Account used for TPM access:/dev/null:/sbin/nologin
systemd-network:x:192:192:systemd Network Management:/:/usr/sbin/nologin
systemd-oom:x:999:999:systemd Userspace OOM Killer:/:/usr/sbin/nologin
systemd-resolve:x:193:193:systemd Resolver:/:/usr/sbin/nologin
polkitd:x:998:997:User for polkitd:/:/sbin/nologin
rpc:x:32:32:Rpcbind Daemon:/var/lib/rpcbind:/sbin/nologin
abrt:x:173:173::/etc/abrt:/sbin/nologin
setroubleshoot:x:997:995:SELinux troubleshoot server:/var/lib/setroubleshoot:/sbin/nologin
cockpit-ws:x:996:994:User for cockpit web service:/nonexisting:/sbin/nologin
cockpit-wsinstance:x:995:993:User for cockpit-ws instances:/nonexisting:/sbin/nologin
rpcuser:x:29:29:RPC Service User:/var/lib/nfs:/sbin/nologin
sshd:x:74:74:Privilege-separated SSH:/usr/share/empty.sshd:/sbin/nologin
chrony:x:994:992::/var/lib/chrony:/sbin/nologin
dnsmasq:x:993:991:Dnsmasq DHCP and DNS server:/var/lib/dnsmasq:/sbin/nologin
tcpdump:x:72:72::/:/sbin/nologin
systemd-coredump:x:989:989:systemd Core Dumper:/:/usr/sbin/nologin
systemd-timesync:x:988:988:systemd Time Synchronization:/:/usr/sbin/nologin
developer:x:1000:1000::/home/developer:/bin/bash
phil:x:1001:1001::/home/phil:/bin/bash
_laurel:x:987:987::/var/log/laurel:/bin/false
```

users: developer, phil


# App.py
lfi to `../app.py` show that websocket is connecting to port 5000 to do orders
it says stuff about dll

by catting /proc/PID/cmdline
can find that the dll is in `/opt/bagel/bin/Debug/net6.0/bagel.dll`
