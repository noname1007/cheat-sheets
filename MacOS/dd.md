# dd

dd (disk dump) is used for bit-precise copying of hard disks, partitions or files.

## Copy iso to USB
to copy a .iso file to an USB stick on Mac OS you have to check the device name of the USB stick e.g. (disk1).
<br></br>
```bash
diskutil list
```
Then you have to unmount the USB stick from your system, copy the file, and eject the USB stick when done.
<br></br>
```bash
# unmount

diskutil unmountDisk /dev/diskN

# copy

sudo dd if=example.iso of=/dev/diskN bs=1m

# eject

diskutil eject /dev/diskN
```