# Alpine Linux on Raspberry Pi Zero 2 W

## Image prep
Download tar  ball from https://alpinelinux.org/downloads/
I used alpine-rpi-3.15.0_rc6-aarch64, armhf does also work


unzip completely to a folder 

Edit config.txt

copy
```
kernel=boot/vmlinuz-rpi
initramfs boot/initramfs-rpi
```
to the `[all]` block, similar to the `[pi3]` block

example:
```
...
[all]
arm_64bit=1
include usercfg.txt
kernel=boot/vmlinuz-rpi
initramfs boot/initramfs-rpi
```


## SD card prep

Use Raspberry Pi imager to prep the SD card with partitions, 1 bootable FAT partition is needed to do the install

After imaging is complete, eject and open the SD card again to replace all imaged files with the files preped above.

## Boot 




### Notes

`lbu commit -d` to save config after `setup-alpine`
