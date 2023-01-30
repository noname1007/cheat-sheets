# Ubuntu phased updates

Phased updates are software updates that are gradually rolled out to users rather than all users getting the updates at the same time.

## Disable

To disable phased updates you have to edit

>/etc/apt/apt.conf.d/99-Phased-Updates

and add these line.
<br></br>
```bash
APT::Get::Always-Include-Phased-Updates True;
```