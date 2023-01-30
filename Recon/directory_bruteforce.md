# Directory bruteforcing

Directory brute forcing is a web application technology used to find and identify possible hidden directories in websites.

## Gobuster

[Gobuster](https://github.com/OJ/gobuster) is a tool used to brute-force URIs including directories and files as well as DNS subdomains.

Usage:
```bash
gobuster dir -u $TARGET -w $WORDLIST -t 50 -x php,txt,html
```

## Feroxbuster

[Feroxbuster](https://github.com/epi052/feroxbuster) is a tool used to brute-force URIs including directories and files as well as DNS subdomains.

Usage:

```bash
./feroxbuster -u $TARGET -x php,txt,html -w $WORDLIST
```