1. What service is running on the target machine over UDP?
	- tftp
2. What class of vulnerability is the webpage that is hosted on port 80 vulnerable to?
	- LFI
1. What is the default system folder that TFTP uses to store files?
	- /var/lib/tftpboot/
2. Which interesting file is located in the web server folder and can be used for Lateral Movement?
	- /htpasswd
3. What is the group that user Mike is a part of and can be exploited for Privilege Escalation?
	-  lxd
4. When using an image to exploit a system via containers, we look for a very small distribution. Our favorite for this task is named after mountains. What is that distribution name?
	- alpine
5. What flag do we set to the container so that it has root privileges on the host system?
	- security.privileged=true
6. If the root filesystem is mounted at /mnt in the container, where can the root flag be found on the container after the host system is mounted?
	- /mnt/root