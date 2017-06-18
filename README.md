# Create-a-Bootable-USB-Flash-Drive-for-Windows-7-8-10-on-MAC-OS-X
Create a Bootable USB Flash Drive for Windows 7/8/10 on MAC OS X


!! Remove the usb flash drive for now !!

***** Step 1 ****
hit space and command at the same time.
-> type terminal

***** Step 2 ****
Type in terminal ( diskutil list ) this well show al the disk what is mounted to your machine.
  ** Note ** Make sure you memorize your usb disk on the left side you well see /dev/disk0 etc.
  
 ***** Step 3 ****
 Here we going to unmount the usb flash drive 
 diskutil unmountDisk /dev/yourusbflashdrive
 -- example (  diskutil unmountDisk /dev/disk2 )
 
  ***** Step 4 ****
Now we going to install the iso in the usb. Make sure you have a Windows ISO 
sudo dd if=yourisofilelocation of=/dev/yourusbflashdrive bs=1m
 -- example ( sudo dd if=/Users/Delgesh/Desktop/Wind10_english_x64.iso of=/dev/disk2 bs=1m)
Enter your user password to contine.

 ***** Step 5 ****
 Wen Step 4 is done we going to eject the usb flash drive
 diskuntil eject /dev/yourusbflashdrive
 -- example ( diskutil eject /dev/disk2 )


Now we succesfull created Bootable USB Flash Drive


