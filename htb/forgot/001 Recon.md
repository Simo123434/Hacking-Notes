
# Nmap
```
22/tcp open  ssh     OpenSSH 8.2p1 Ubuntu 4ubuntu0.5 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   3072 48add5b83a9fbcbef7e8201ef6bfdeae (RSA)
|   256 b7896c0b20ed49b2c1867c2992741c1f (ECDSA)
|_  256 18cd9d08a621a8b8b6f79f8d405154fb (ED25519)
80/tcp open  http    Werkzeug/2.1.2 Python/3.8.10
|_http-title: Login
| fingerprint-strings: 
|   FourOhFourRequest: 
|     HTTP/1.1 404 NOT FOUND
|     Server: Werkzeug/2.1.2 Python/3.8.10
|     Date: Wed, 01 Mar 2023 01:25:54 GMT
|     Content-Type: text/html; charset=utf-8
|     Content-Length: 207
|     X-Varnish: 2857369
|     Age: 0
|     Via: 1.1 varnish (Varnish/6.2)
|     Connection: close
|     <!doctype html>
|     <html lang=en>
|     <title>404 Not Found</title>
|     <h1>Not Found</h1>
|     <p>The requested URL was not found on the server. If you entered the URL manually please check your spelling and try again.</p>
|   GetRequest: 
|     HTTP/1.1 302 FOUND
|     Server: Werkzeug/2.1.2 Python/3.8.10
|     Date: Wed, 01 Mar 2023 01:25:48 GMT
|     Content-Type: text/html; charset=utf-8
|     Content-Length: 219
|     Location: http://127.0.0.1
|     X-Varnish: 528685
|     Age: 0
|     Via: 1.1 varnish (Varnish/6.2)
|     Connection: close
|     <!doctype html>
|     <html lang=en>
|     <title>Redirecting...</title>
|     <h1>Redirecting...</h1>
|     <p>You should be redirected automatically to the target URL: <a href="http://127.0.0.1">http://127.0.0.1</a>. If not, click the link.
|   HTTPOptions: 
|     HTTP/1.1 200 OK
|     Server: Werkzeug/2.1.2 Python/3.8.10
|     Date: Wed, 01 Mar 2023 01:25:48 GMT
|     Content-Type: text/html; charset=utf-8
|     Allow: HEAD, OPTIONS, GET
|     Content-Length: 0
|     X-Varnish: 2857365
|     Age: 0
|     Via: 1.1 varnish (Varnish/6.2)
|     Accept-Ranges: bytes
|     Connection: close
|   RTSPRequest, SIPOptions: 
|_    HTTP/1.1 400 Bad Request
|_http-server-header: Werkzeug/2.1.2 Python/3.8.10
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port80-TCP:V=7.93%I=7%D=3/1%Time=63FEA998%P=x86_64-pc-linux-gnu%r(GetRe
SF:quest,1E3,"HTTP/1\.1\x20302\x20FOUND\r\nServer:\x20Werkzeug/2\.1\.2\x20
SF:Python/3\.8\.10\r\nDate:\x20Wed,\x2001\x20Mar\x202023\x2001:25:48\x20GM
SF:T\r\nContent-Type:\x20text/html;\x20charset=utf-8\r\nContent-Length:\x2
SF:0219\r\nLocation:\x20http://127\.0\.0\.1\r\nX-Varnish:\x20528685\r\nAge
SF::\x200\r\nVia:\x201\.1\x20varnish\x20\(Varnish/6\.2\)\r\nConnection:\x2
SF:0close\r\n\r\n<!doctype\x20html>\n<html\x20lang=en>\n<title>Redirecting
SF:\.\.\.</title>\n<h1>Redirecting\.\.\.</h1>\n<p>You\x20should\x20be\x20r
SF:edirected\x20automatically\x20to\x20the\x20target\x20URL:\x20<a\x20href
SF:=\"http://127\.0\.0\.1\">http://127\.0\.0\.1</a>\.\x20If\x20not,\x20cli
SF:ck\x20the\x20link\.\n")%r(HTTPOptions,119,"HTTP/1\.1\x20200\x20OK\r\nSe
SF:rver:\x20Werkzeug/2\.1\.2\x20Python/3\.8\.10\r\nDate:\x20Wed,\x2001\x20
SF:Mar\x202023\x2001:25:48\x20GMT\r\nContent-Type:\x20text/html;\x20charse
SF:t=utf-8\r\nAllow:\x20HEAD,\x20OPTIONS,\x20GET\r\nContent-Length:\x200\r
SF:\nX-Varnish:\x202857365\r\nAge:\x200\r\nVia:\x201\.1\x20varnish\x20\(Va
SF:rnish/6\.2\)\r\nAccept-Ranges:\x20bytes\r\nConnection:\x20close\r\n\r\n
SF:")%r(RTSPRequest,1C,"HTTP/1\.1\x20400\x20Bad\x20Request\r\n\r\n")%r(Fou
SF:rOhFourRequest,1C0,"HTTP/1\.1\x20404\x20NOT\x20FOUND\r\nServer:\x20Werk
SF:zeug/2\.1\.2\x20Python/3\.8\.10\r\nDate:\x20Wed,\x2001\x20Mar\x202023\x
SF:2001:25:54\x20GMT\r\nContent-Type:\x20text/html;\x20charset=utf-8\r\nCo
SF:ntent-Length:\x20207\r\nX-Varnish:\x202857369\r\nAge:\x200\r\nVia:\x201
SF:\.1\x20varnish\x20\(Varnish/6\.2\)\r\nConnection:\x20close\r\n\r\n<!doc
SF:type\x20html>\n<html\x20lang=en>\n<title>404\x20Not\x20Found</title>\n<
SF:h1>Not\x20Found</h1>\n<p>The\x20requested\x20URL\x20was\x20not\x20found
SF:\x20on\x20the\x20server\.\x20If\x20you\x20entered\x20the\x20URL\x20manu
SF:ally\x20please\x20check\x20your\x20spelling\x20and\x20try\x20again\.</p
SF:>\n")%r(SIPOptions,1C,"HTTP/1\.1\x20400\x20Bad\x20Request\r\n\r\n");
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 156.75 seconds

```

# Web
page is a login page
other pages -> forgot
reset -> invalid token

login page has comment in source code:  **robert-dev-367120**

by changing the host header in the forgot request we can capture the token of the reset request and change the password.


