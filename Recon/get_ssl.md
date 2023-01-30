# SSL cert

## get SSL cert
```bash
openssl s_client -connect 127.0.0.1:443

# copy base64 encoded cert and press "Q" to exit

# paste base64 encoded cert to file

openssl -x509 -in file.cert -noout -text
