# HOW TO ROOT ONEPLUS NORD
[source](https://forum.xda-developers.com/t/guide-how-to-root-oneplus-nord.4139411)

1. Download Firmware Image Zip
   - [Firmware Image](https://forum.xda-developers.com/t/oneplus-nord-rom-ota-oxygen-os-repo-of-oxygen-os-builds.4138085)

2. Dump boot.img with payload_dumper-win64
   - payload_dumper-win64.exe
   - [payload_dumper](https://gist.github.com/ius/42bd02a5df2226633a342ab7a9c60f15)

3. Patch boot.img with Magisk

4. Copy patched boot.img to pc & Patch with fastboot
```sh
adb reboot bootloader

fastboot flash boot_a magisk_patched-23001_QuVY0.img 
fastboot flash boot_b magisk_patched-23001_QuVY0.img 
```
