# Adding a New Hard Drive

While adding a new hard drive into your desktop may seem daunting, it is actually quite simple. This short guide will give you step by step instructions on how to install a brand new hard drive into a pre-existing desktop. 

## What you need
- A working desktop
- A new hard drive
- Available hard drive tray
- SATA cable
- Optional: mounting bracket

## Installing the hard drive to your computer:
1.	Turn off your desktop. Toggle the power switch on the desktop off, and then unplug all cables and wires connected to it.
2.	Remove the desktop case’s side covers. You should be able to see the machine’s motherboard and hard drive(s).
3.	Remove an empty hard drive tray.
4.	Install your new hard drive onto the hard drive tray.
    - If you have a mounting bracket, install the hard drive onto the mounting bracket first, then install the mounting bracket onto the hard drive tray.
5.	Place the hard drive tray with the new hard drive back in.
6.	Find your desktop’s SATA power cable and connect it to your new hard drive. 
7.	Connect your SATA cable to the motherboard and new hard drive’s SATA ports. Make sure you have enough space to put back the side covers.
8.	Put the side covers back onto the computer case. Ensure they are secure.
9.	Plug back in the power and peripheral cables.


## Setting up the hard drive:
After installing the new hard drive, you will need to format and partition the disk before you can use it. How to do so will vary based on your desktop’s operating system. 

###   Windows
1.	Open the control panel. 
2.	From the control panel, open administrative tools.
3.	Open computer management.
4.	Open disk management.
5.	Choose the option “GPT (GUID Partition Table)” and click “OK.”
6.	In the computer management screen, you should see a new disk with unallocated space.  Right-click the disk and choose “New Simple Volume.”
7.	Click “Next” until you must assign the drive a letter. Choose any letter from the dropdown and then click “Next”.
8.	Choose “NTFS” for File System, “Default” for Allocation Unit Size, and enter a name for Volume Label. Leave “Perform a quick format” checked.
9.	Click “Next”, and then click “Finish”.

### Linux
1.	Open a terminal and run the command ```sudo lshw –C disk```
    - You should see output listing out disk information
2.	Take note of the Logical Name entry for your new hard drive.
3.	Open the GParted application
    - If you do not have it installed on your computer, first install it by running the command ```sudo apt-get install gparted```
4.	In the top right corner of the application, choose your new hard drive from the drop-down list. You may have to refer back to the Logical Name from earlier.
5.	Right-click on the gray bar across the top with the text, “unallocated,” and choose ‘New.’
6.	You can generally leave most settings at their default value here. However, you must choose a file system to use.
    - Choose ext3 if you will only use Linux on this computer. Choose fat32 if you will use both Linux and Windows on this computer.
7.	Next to Label, enter a name for your new hard drive.
8.	Click “Add”.
9.	Click “Apply All Operations”, and wait for the disk to be partitioned and formatted. 

