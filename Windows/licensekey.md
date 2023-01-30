# Windows license key

A way to read out the Windows license key stored in the ACPI-Firmware.

## Linux

On a Linux host type in your commandline

```bash
sudo strings '/sys/firmware/acpi/tables/MSDM'
```
## Windows

On a Windows host type in powershell
```powershell
(Get-WmiObject -query &apos;select * from SoftwareLicensingService&apos;).OA3xOriginalProductKey
```