# Upgrade shell

A way to upgrade a low privileged shell like netcat is to use python.

## Usage:

```bash
# check if python is installed

which python

# spawn bash
python -c 'import pty; pty.spawn("/bin/bash")'

export TERM=xterm-256color

^Z # background shell an stabilize

stty size

stty raw -echo ; fg ; reset

stty rows 200

stty cols 200
```