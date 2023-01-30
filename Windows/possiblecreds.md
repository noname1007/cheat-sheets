# Possible locations for Creds

## Autologon:
reg query "HKLM\SOFTWARE\Microsoft\Windows NT\Currentversion\Winlogon"

## VNC:
reg query "HKCU\Software\ORL\WinVNC3\Password"

## Putty:
reg query "HKCU\Software\SimonTatham\PuTTY\Sessions"