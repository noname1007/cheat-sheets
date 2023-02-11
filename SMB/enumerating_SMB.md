# Enumerating SMB

[Server Message Block](https://en.wikipedia.org/wiki/Server_Message_Block) is a communication protocol originally developed in 1983 by Barry A. Feigenbaum at IBM and intended to provide shared access to files and printers across nodes on a network of systems running IBM's OS/2.

## enum4linux

[Enum4linux](https://labs.portcullis.co.uk/application/enum4linux/) is a tool for enumerating information from Windows and Samba systems.

Usage:
```bash

enum4linux [options] $IP

-U             get userlist
-M             get machine list
-N             get namelist dump (different from -U and-M)
-S             get sharelist
-P             get password policy information
-G             get group and member list

-a             all of the above (full basic enumeration)
```
## Nmap
We can use nmap scripts to enumerate SMB.
```bash
nmap -p [PORT] --script=smb-enum-shares.nse,smb-enum-users.nse [IP]
```

## Smbclient

When the following conditions are met,

    - we know the SMB share location

    - we know the name of an interesting SMB share

we can use smbclient to try log in to the target maschine as user "Anonymous" without providing a password.

```bash
smbclient //[IP]/[SHARE] [OPTIONS]

	-U [name] : to specify the user

	-p [port] : to specify the port

smbclient //10.10.10.2/secret -U user -p 445
```
To download a complete share we can use smbget.
```bash
smbget -R smb://[IP]/[SHARE]
```