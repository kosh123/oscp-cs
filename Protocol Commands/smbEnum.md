# Enumerating SMB

### Nmap

Using nmap, the following commands can be used:
nmap -p445 — script smb-protocols <target ip>
nmap -p139 — script smb-protocols <target ip>

Note: the ‘-sV’ and the ‘-sC’ tag can be used to run nmap automated scripts against SMB for enumeration as well. 

### SMBMap
#### Allows users to enumerate samba share drives across a domain.

smbmap -H \<target IP\>

smbmap -H \<target IP\> -d \<target domain\> -u \<user\> -p \<password\>


### SMBClient
