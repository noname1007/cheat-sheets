# Enumerating SMTP

The [Simple Mail Transfer Protocol](https://en.wikipedia.org/wiki/Simple_Mail_Transfer_Protocol) is an Internet standard communication protocol for electronic mail transmission.

## smtp-user-enum

[smtp-user-enum](http://pentestmonkey.net/tools/user-enumeration/smtp-user-enum) is a username guessing tool primarily for use against the default Solaris SMTP service. Can use either EXPN, VRFY or RCPT TO.

```bash
smtp-user-enum -h

smtp-user-enum -M VRFY -U users.txt -t $IP
smtp-user-enum -M EXPN -u admin1 -t $IP
smtp-user-enum -M RCPT -U users.txt -T mail-server-ips.txt
smtp-user-enum -M EXPN -D example.com -U users.txt -t $IP
```
## Metasploit

```bash
# start metasploit

msfconsole

# search module

search smtp_version

# set module, options and run

use auxiliary/scanner/smtp/smtp_version

show options

exploit

search module

search smtp_enum

# set module, options and run

use auxiliary/scanner/smtp/smtp_enum

show options

# useful list  /usr/share/wordlists/SecLists/Usernames/top-usernames-shortlist.txt

exploit
```