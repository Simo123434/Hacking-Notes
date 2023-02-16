Nmap scan
```
Starting Nmap 7.92 ( https://nmap.org ) at 2023-01-31 18:27 AEST
Nmap scan report for stocker.htb (10.10.11.196)
Host is up (0.65s latency).
Not shown: 998 closed tcp ports (conn-refused)
PORT   STATE SERVICE VERSION
22/tcp open  ssh     OpenSSH 8.2p1 Ubuntu 4ubuntu0.5 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   3072 3d:12:97:1d:86:bc:16:16:83:60:8f:4f:06:e6:d5:4e (RSA)
|   256 7c:4d:1a:78:68:ce:12:00:df:49:10:37:f9:ad:17:4f (ECDSA)
|_  256 dd:97:80:50:a5:ba:cd:7d:55:e8:27:ed:28:fd:aa:3b (ED25519)
80/tcp open  http    nginx 1.18.0 (Ubuntu)
|_http-generator: Eleventy v2.0.0
|_http-title: Stock - Coming Soon!
|_http-server-header: nginx/1.18.0 (Ubuntu)
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
```

web basic page
**Angoose Garden,** Head of IT at Stockers Ltd.


gobuster vhost:
```
gobuster vhost -u http://stocker.htb/ -w /usr/share/seclists/Discovery/DNS/bitquark-subdomains-top100000.txt 
```
finds **dev.stocker.htb**