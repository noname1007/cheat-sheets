# Open ports
To show all open ports on Mac OS use these options.

## TCP

to show all open TCP ports on your Mac OS type

```bash
lsof -n -i4TCP -P

# or

sudo lsof -i -P | grep LISTEN | grep :$PORT
```

## UDP

to show all open UDP ports on your Mac OS type

```bash
lsof -n -i4UDP -P

# or

sudo lsof -i -P | grep LISTEN | grep :$PORT
```