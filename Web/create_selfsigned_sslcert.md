# Create SSL cert

To create a self signet SSL cert on a linux host type

```bash
openssl req -x509 -newkey rsa:4096 -keyout key.pem -out cert.pem -sha256 -days 365
```