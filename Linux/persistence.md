# Persistence

This are some common persistence mechanisms for Linux to look for in post-exploitation.

## Locations

Adding e.g. a reverse shell in these locations will ensure a way back if a connection is lost.

```bash
/etc/rc.local
/etc/init.d/
/etc/profile
/etc/crontab
/etc/cron.d/
/etc/cron.hourly/
/etc/cron.daily/
/etc/cron.weekly/
/etc/cron.monthly/
/etc/cron.yearly/
Startup Applications
Systemd Services
.bashrc
.bash_profile
.bash_logout
```