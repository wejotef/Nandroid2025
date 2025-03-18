# Nandroid2025
A Nandroid Backup solution using ADB coded as a Windows batchfile



Purpose

The script automates the process of creating a Nandroid backup of an Android device. A Nandroid backup is a complete snapshot of your device's software, including the operating system, applications, data, and settings. This allows you to restore your device to a previous state in case of software issues.    

Requirements

Android Device: The device must be rooted (unless it's a pre-rooted build).
Windows 11 or higher: The script is designed for Windows 11 or newer.    
ADB (Android Debug Bridge): ADB must be installed and accessible on your computer.    
Sufficient Disk Space: Ensure you have enough free space on your PC to store the backup. The script attempts to estimate the required space.    

Setup

Install ADB: If you haven't already, download and install the Android Debug Bridge (ADB) on your computer. You'll also need to ensure that ADB is added to your system's PATH environment variable so that you can execute adb commands from any command prompt window.
Enable USB Debugging: On your Android device, enable USB debugging in the developer options.
Connect Your Device: Connect your Android device to your computer using a USB cable.

Set Backup Location:
Open the script file (e.g., nandroid.bat) in a text editor.
Modify the line set "PC_BACKUP_DIR=E:\Nandroid2025" to specify the directory on your PC where you want to store the backups. For example: set "PC_BACKUP_DIR=D:\MyNandroidBackups

Set ADB Path (If Necessary):
If the script cannot automatically find your ADB installation, you may need to set the path manually.
Modify the line set "ADB=C:\ADB\adb.exe" to point to the correct location of your adb.exe file. For example: set "ADB=C:\Program Files (x86)\Android\platform-tools\adb.exe"    

How to Run the Backup

Open a Command Prompt: Open a command prompt window.
Navigate to the Script's Directory: Use the cd command to navigate to the directory where you saved the nandroid.bat file.
Run the Script: Execute the script by typing nandroid.bat and pressing Enter.

Follow the Prompts: The script will guide you through the backup process. It will perform several checks, such as verifying your device connection, checking for root access, and estimating disk space.    

Command Line Options

The script supports a few command-line options to customize the backup process:

-d: Decrypt files in the /userdata partition. This is useful for backing up user data in a usable format on devices with File-Based Encryption (FBE).   

-x <directories>: Exclude specific directories from the /userdata partition backup. <directories> should be a semi-colon separated list of directory names. For example: nandroid.bat -x Downloads;DCIM.    

-c: Create a TAR archive of the backup files instead of raw images.


Screenshot
![Screenshot 2025-03-17 153012](https://github.com/user-attachments/assets/7b0b662a-10c6-4f90-b522-2f48ba3ac9d3)
