# NetworkManager

[NetworkManager](https://wiki.gnome.org/Projects/NetworkManager) is a program for providing detection and configuration for systems to automatically connect to networks.

## MAC randomization

To change your MAC address every time a connection is establishing create 

>/etc/NetworkManager/conf.d/50-macchange.conf

and add the following lines.
<br></br>
```bash
[connection-mac-randomization]
ethernet.cloned-mac-address=random
wifi.cloned-mac-address=random
```

## Hostname

To avoid that your hostname is send to the network you have to edit
>/etc/NetworkManager/NetworkManager.conf

and add the following lines.
<br></br>
```bash
[ipv4]
dhcp-send-hostname=false
```