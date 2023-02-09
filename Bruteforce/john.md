# John the Ripper

[John the Ripper](https://www.openwall.com/john/) is a free password cracking software tool.

## Cracking basic hashes

To crack basic hashes you need to identify it first. Ypo can use tools like name-the-hash for this. The syntax to crack the hash using john is.

```bash
john --format=[FORMAT] --wordlist=[WORDLIST] [FILE]
```

## Cracking Windows Hashes
NThash is the hash format that modern Windows Operating System machines will store user and service passwords in. It's also commonly referred to as "NTLM" which references the previous version of Windows format for hashing passwords known as "LM", thus "NT/LM". To crack it, use
```bash
john --format=nt --wordlist=[WORDLIST] [FILE]
```

## /etc/shadow
The /etc/shadow file is the file on Linux machines where password hashes are stored. To crack it, we need first to 'unshadow' it. John the Ripper has a builtin function for that.
```bash
unshadow [path to passwd] [path to shadow] > unshadow.txt
```
Then we can crack it like any other hash using John.
```bash
john --wordlist=[WORDLIST] --format=sha512crypt unshadow.txt
```

## Cracking a Password Protected Zip File
To crack password protected zip files, we need first to convert it to a format John can work with by using 'zip2john'.
```bash
zip2john [OPTIONS] [ZIP FILE] > [OUTPUT]
```
Then we can crack it like any other hash using John.
```bash
john --wordlist=[WORDLIST] [FILE]
```

## Cracking a Password Protected RAR Archive
To crack password protected rar archives, we need first to convert it to a format John can work with by using 'rar2john'.
```bash
rar2john [OPTIONS] [RAR FILE] > [OUTPUT]
```
Then we can crack it like any other hash using John.
```bash
john --wordlist=[WORDLIST] [FILE]
```

## Cracking SSH Key Passwords
To crack password protected ssh keys, we need first to convert it to a format John can work with by using 'ssh2john'.

```bash
ssh2john [id_rsa] > [OUTPUT]
```
Then we can crack it like any other hash using John.
```bash
john --wordlist=[WORDLIST] [FILE]
```