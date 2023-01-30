# Subdomain bruteforcing

What is DNS bruteforcing? It's a technique where the person takes a long list of common subdomain names and append their target to them and based on the response determines whether they are valid or not.

## Gobuster
```bash
gobuster vhost -k -u $TARGET -w $WORDLIST --append-domain
```
## Amass
```bash
# OSINT passive scan

amass enum -d $TARGET
````