# Anonymous FTP login

On some systems FTP is so configured to  let you log in as user 'Anonymous' without a password.

## Try login

Try to login as user 'Anonymous' without providing a password
<br></br>
```
ftp [IP]
```

## Bruteforce FTP
When the following conditions are met,

    - There is an FTP server running on the target machine

    - We have a possible username

we can try to bruteforce the FTP service with [hydra](https://github.com/vanhauser-thc/thc-hydra).
<br></br>
```
hydra -t 4 -l [USER] -P [WORDLIST] -vV [IP] ftp
```
