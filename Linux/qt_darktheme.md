# Ubuntu qt darktheme

GTK themes does sometimes not work properly on Qt Startup Applications.

## Workaround

To enable dark theme in qt applications like e.g. Wireshark, you have to install adwaita-qt, a Qt 5 port of GNOME’s Adwaita theme.
<br></br>
```bash
sudo apt install -y adwaita-qt
```
Then you could alias one of these 2 options to run your application in dark mode.
<br></br>
```bash
QT_STYLE_OVERRIDE=Adwaita-Dark [APPLICATION]

[APPLICATION] -style Adwaita-Dark
```