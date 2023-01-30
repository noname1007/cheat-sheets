# ICMP listener

A example how to setup a ICMP listener to check code execution on target with pings.

## Example:
```bash
# on host

sudo tcpdump ip proto \\icmp -i $INTERFACE

# on target

ping -c 1 $HOST

```