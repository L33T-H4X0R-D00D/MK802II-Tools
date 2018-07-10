# MK802II-Tools
This is not the only way to configure an MK802II to run GNU/Linux or specifially Linaro. This is the method I've developed which has made it easiest to be supported by junior admins for use as lobby signage, and lite workstations.

# Files included
* REAME.md - This file. Inventory and instructions for prep and install.
* Display Modes.7z - Contains pre-configured EVB.BIN files in popular HD formats. (720p@50Hz, 720p@60Hz, 1080p@24Hz, 1080i@50Hz, 1080p@50Hz, 1080i@60Hz, 1080p@60Hz)
* OS Image - The core linux image which these documents build from. You will need to download all 3 files to unzip the image file to 
* windiskimager.7z - Used to burn image files to SD card. Version 0.6 is included here but a newer version may work if you're so inclined.



# Requirements

* Working windows machine
* MK802II device
* 8gig or larger microSD card
* Usb MicroSD card reader
* 7zip
* Wireless 802.11a/b/g/n connection to the internet.

The system password is "linaro".  

# First boot and initial setup.

1. On a windows machine, plug the microSD card reader into an open USB slot.
2. Insert the microSD card into the microSD card reader. Note: All data currently on this card will be overwritten during setup. Make sure you have backed up any important data on the card before continuing. 
3. Using 7zip, unzip linaro-alip-armhf-t4-1080p.zip on the desktop.
4. Using 7zip, unzip windiskimager.zip on the desktop. 
5. Double click on the windiskimager folder on the desktop. 
6. Double click Win32DiskImager.exe. 
7. If the UAC appears, click YES.
8. Click the folder icon to the right of the image file text box. 
9. In the window that opens, navigate to the desktop and select linaro-alip-armhf-t4-1080p.img.
10. Click the drop down box under the device heading and select the microSD card. 
11. Click the “Write” button. 
12. A box will appear warning you that all data on the SD card will be overwritten. Click “YES”. The write process can take anywhere from 5 – 45 minutes depending on the speed of your SD card. 
13. After the write has been completed a box will appear to alert you. Click “OK”.
14. Close Win32DiskImager.
15. Double click My Computer.
16. Double click on the microSD card. 
17. You should see 3 files. evb.bin, script.bin and uImage. 
18. Using 7zip, unzip Display Modes.zip to the desktop.
19. Select the evb file that matches a resolution your display device supports. Note: most 1080p display devices support 1920x1080x24hz.
20. Rename the file you selected to evb.bin.
21. Move the file you just renamed to the microSD card.
22. Windows will alert you that you’re about to overwrite a file. Click “overwrite”. 
23. Install the SD card in the MK802II device.
24. Connect a keyboard and mouse to the two USB ports on the MK802II device.
25. Plug the MK802II device into a monitor/tv HDMI port. If you’re using a TV make certain the aspect ratio is set to 1:1, full or computer mode. Make certain to use the HDMI extension cable to prevent overheating of the MK802II device. 
26. Connect the USB cable plugged into the power port on the MK802II to a USB port on the TV/Monitor.  The Linaro OS will boot and log in to the desktop. 
27. Give the device several minutes after the desktop first appears and then hit CTRL + ALT + T.  A command prompt will open. 
28. Type "sudo shutdown -r now" and hit enter.  The machine will reboot and then return to the desktop. 
29. In the bottom right corner there is a circular spinning icon that eventually turns into the wireless network icon. Click it once. 
30. A small menu will open displaying a list of the available wireless networks. Click the network you wish to use. 
31. The device will ask you to provide the system password.
32. Right click the same wireless network icon you chose in the previous step, then click "edit connections".
33. The device will ask you to provide the system password.
34. Click the wireless tab. 
35. Click the name of the wireless network you chose in step 10.  Then click edit.
36. The device will ask you to provide the system password. 
37. Click the wireless security tab.
38. Select the type of security your wireless network uses then enter the wireless network password below.
39. Click save. 
40. Click close.


