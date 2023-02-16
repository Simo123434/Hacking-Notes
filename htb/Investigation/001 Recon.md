# Nmap
```
Nmap scan report for 10.10.11.197
Host is up (0.58s latency).
Not shown: 997 closed tcp ports (reset)
PORT      STATE SERVICE VERSION
22/tcp    open  ssh     OpenSSH 8.2p1 Ubuntu 4ubuntu0.5 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   3072 2f:1e:63:06:aa:6e:bb:cc:0d:19:d4:15:26:74:c6:d9 (RSA)
|   256 27:45:20:ad:d2:fa:a7:3a:83:73:d9:7c:79:ab:f3:0b (ECDSA)
|_  256 42:45:eb:91:6e:21:02:06:17:b2:74:8b:c5:83:4f:e0 (ED25519)
80/tcp    open  http    Apache httpd 2.4.41
	|_http-title: Did not follow redirect to http://eforenzics.htb/
|_http-server-header: Apache/2.4.41 (Ubuntu)
31337/tcp open  Elite?
| fingerprint-strings: 
|   DNSStatusRequestTCP, DNSVersionBindReqTCP, FourOhFourRequest, GenericLines, GetRequest, HTTPOptions, Help, NULL, RPCCheck, RTSPRequest, TerminalServerCookie, X11Probe: 
|     BRev
|_    should not see this message, please download the client from https://github.com/borzacchiello/brev
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port31337-TCP:V=7.92%I=7%D=2/7%Time=63E2546F%P=x86_64-pc-linux-gnu%r(NU
SF:LL,6E,"\nBRev\n\nYou\x20should\x20not\x20see\x20this\x20message,\x20ple
SF:ase\x20download\x20the\x20client\x20from\x20https://github\.com/borzacc
SF:hiello/brev\n")%r(GetRequest,6E,"\nBRev\n\nYou\x20should\x20not\x20see\
SF:x20this\x20message,\x20please\x20download\x20the\x20client\x20from\x20h
SF:ttps://github\.com/borzacchiello/brev\n")%r(GenericLines,6E,"\nBRev\n\n
SF:You\x20should\x20not\x20see\x20this\x20message,\x20please\x20download\x
SF:20the\x20client\x20from\x20https://github\.com/borzacchiello/brev\n")%r
SF:(HTTPOptions,6E,"\nBRev\n\nYou\x20should\x20not\x20see\x20this\x20messa
SF:ge,\x20please\x20download\x20the\x20client\x20from\x20https://github\.c
SF:om/borzacchiello/brev\n")%r(RTSPRequest,6E,"\nBRev\n\nYou\x20should\x20
SF:not\x20see\x20this\x20message,\x20please\x20download\x20the\x20client\x
SF:20from\x20https://github\.com/borzacchiello/brev\n")%r(RPCCheck,6E,"\nB
SF:Rev\n\nYou\x20should\x20not\x20see\x20this\x20message,\x20please\x20dow
SF:nload\x20the\x20client\x20from\x20https://github\.com/borzacchiello/bre
SF:v\n")%r(DNSVersionBindReqTCP,6E,"\nBRev\n\nYou\x20should\x20not\x20see\
SF:x20this\x20message,\x20please\x20download\x20the\x20client\x20from\x20h
SF:ttps://github\.com/borzacchiello/brev\n")%r(DNSStatusRequestTCP,6E,"\nB
SF:Rev\n\nYou\x20should\x20not\x20see\x20this\x20message,\x20please\x20dow
SF:nload\x20the\x20client\x20from\x20https://github\.com/borzacchiello/bre
SF:v\n")%r(Help,6E,"\nBRev\n\nYou\x20should\x20not\x20see\x20this\x20messa
SF:ge,\x20please\x20download\x20the\x20client\x20from\x20https://github\.c
SF:om/borzacchiello/brev\n")%r(TerminalServerCookie,6E,"\nBRev\n\nYou\x20s
SF:hould\x20not\x20see\x20this\x20message,\x20please\x20download\x20the\x2
SF:0client\x20from\x20https://github\.com/borzacchiello/brev\n")%r(X11Prob
SF:e,6E,"\nBRev\n\nYou\x20should\x20not\x20see\x20this\x20message,\x20plea
SF:se\x20download\x20the\x20client\x20from\x20https://github\.com/borzacch
SF:iello/brev\n")%r(FourOhFourRequest,6E,"\nBRev\n\nYou\x20should\x20not\x
SF:20see\x20this\x20message,\x20please\x20download\x20the\x20client\x20fro
SF:m\x20https://github\.com/borzacchiello/brev\n");
Service Info: Host: eforenzics.htb; OS: Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 71.25 seconds

```

port 80 webpage is `eforenzics.htb`

other webpages is service.html
upload jpg which is read by exiftool 12.37

exiftool 12.37 has pipe vulnerability

create html page with bash reverse shell

start nc and upload payload image