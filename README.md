# HTB-Nibble
Machine Hack the box Nibble
![alt text](image.png)

## RECON

**Nmap**

**2 TCP ports opens**

Discovered open port 22/tcp on 10.10.10.75
Discovered open port 80/tcp on 10.10.10.75
***************
**Services**
22/tcp open  ssh     syn-ack OpenSSH 7.2p2 Ubuntu 4ubuntu2.2 (Ubuntu Linux; protocol 2.0)

80/tcp open  http    syn-ack Apache httpd 2.4.18 ((Ubuntu))


**Check the Website** 

![alt text](image-1.png)


I check source code


![alt text](image-3.png)

 **!!Web blog¡¡** 

 ![alt text](image-4.png)

try to find an exploit to nibbleblog

## EXPLOIT

**I find one exploit in a metasploit module**

![alt text](image-6.png)




and explore to subdomains

![alt text](image-7.png)

**admin.php**

and ask for user 

we finf user,xml 

![alt text](image-8.png)


we try password **nibbles**

we find the version of the nibbleblog
![alt text](image-9.png)

we fins  a Vulnerability 

![alt text](image-10.png)

Use the metasploit exploit 

![alt text](image-11.png)

use user flag 

![alt text](image-12.png)

Find out a script to priv escalation 

![alt text](image-13.png)

We temper the script to revesrse shell and liset to nc port 


![alt text](image-14.png)


![alt text](image-15.png)

Im root 💀

![alt text](image-16.png)