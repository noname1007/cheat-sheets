# USBGuard

The [USBGuard](https://usbguard.github.io/) software framework helps to protect your computer against rogue USB devices (a.k.a. BadUSB) by implementing basic whitelisting and blacklisting capabilities based on device attributes.

## Install

To install USBGuard on Debian based distributions, type

```bash
sudo apt install -y usbguard

# generate basic config

sudo usbguard generate-policy > rules.conf

sudo cp rules.conf /etc/usbguard/rules.conf
sudo chmod 0600 /etc/usbguard/rules.conf

# change this settings in /etc/usbguard/usbguard-daemon.conf

PresentDevicePolicy		= apply-policy
PresentControllerPolicy = apply-policy

# start service

systemctl start usbguard
```
## Management

USB device managment is simple as,

```bash
# to show all devices

usbguard list-devices

# to allow a device

usbguard allow-device [ID]

# or to allow permanent

usbguard allow-device --permanent [ID]
```