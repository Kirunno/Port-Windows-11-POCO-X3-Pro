<img align="right" src="https://github.com/woa-vayu/src_vayu_windows/blob/main/2Poco X3 Pro Windows.png" width="350" alt="Windows 11 Running On A Poco X3 Pro">

# Running Windows on the POCO X3 Pro

## Dualbooting Android and Windows seamlessly

### Prerequisites
- A rooted vayu with Windows already installed
- [UEFI image](https://github.com/woa-vayu/POCOX3Pro-Releases/releases/latest)
- [M3K Helper](https://github.com/woa-vayu/WoA-Helper-M3K/releases/latest)
- [StA Installer](https://github.com/woa-vayu/POCOX3Pro-Guides/raw/main/Files/StA_Installer_vayu.exe)

## Setting up the dualboot app
> This guide assumes you are rooted, if you aren't, please do this first

### Setup - Android
- Download and install the **M3K Helper** app, then open it and grant it root access.
- Download the **UEFI image** for your panel and place it inside the folder named `UEFI` in your internal storage.
- Press the `MOUNT WINDOWS` button, then download and move **StA_Installer_vayu.exe** to the newly created `Windows` folder in your internal storage.
- Return to the M3K Helper app and press `QUICKBOOT TO WINDOWS`.
  
> [!NOTE]
> The first Windows boot can take up to 10 minutes, don't worry and just wait

### Setup - Windows
- Navigate to `C:\StA_Installer_vayu.exe` and run it. If it doesn't work, make sure that any antivirus software is off, as it will probably not let the app run

#### Booting to Android
- Run the new shortcut on your desktop (you can also pin it to your start menu / taskbar for ease of access)

#### Booting to Windows
- Press `QUICKBOOT TO WINDOWS` inside the app, or use the newly created toggle in your quick settings panel
  
## Finished!




















