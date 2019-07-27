# Optiplex-3050-OSX86
Clover Hackintosh EFI files for Dell Optiplex-3050

This is a project created for my office dell computer , supported macOS high sierra 10.13.6 and below

Installed at 2018-09-26 , works totally fine until now


Updates:
2019-09-27 upgraded to mojave 10.14.6 with a little help from 
https://www.tonymacx86.com/threads/mojave-10-14-5-on-dell-optiplex-3050.279277/

1.Modify BIOS settings use efi shell

Prepare a USB Flash drive formatted as FAT32, download refi.zip, Unzip and place it in the root directory of the USB Flash drive.
Boot from the USB Flash drive in UEFI model and you can go into GRUB interface.

Type setup_var 0x795 0x2, then Enter. Change DVMT to 64MB.
Type setup_var 0x4ed 0x0, then Enter. Disable CFG Lock to prevent MSR 0x02 errors on boot.
2.Download clover.zip and install Mojave like usual

the native power management of CPU and GPU load normally. I fake ALC255(3234) ID 11. The outputs are perfect and the headset mic need ComboJack to drive.

I use a HDMI to VGA adapter. The only question is that it can't awake after sleep. Maybe relating to the USB port, because I didn't create a custom SSDT for USBInjectAll.kext like Rehabman's advise lacking of a USB3.0 Flash drive. I want you guys can do me a favor creating this SSDT and sharing it. Thank you!
