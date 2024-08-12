# Updating Drivers and UEFI firmware

Table of Contents:

1. [Files/Tools needed 📃](#filestools-needed-📃)
2. [Steps 🛠️](#steps-🛠️)

## Files/Tools needed 📃

- You will need the following files from the [BSP Release page](https://github.com/woa-vayu/POCOX3Pro-Releases/releases/latest):

UEFI Image:

| File Name                              |
|----------------------------------------|
| POCO.X3.Pro.UEFI-v2XXX.XX.img          |

Windows Drivers:

| File Name                                       |
|-------------------------------------------------|
| POCOX3Pro-Drivers-v2XXX.XX-Desktop.7z           |

TWRP image:

| File Name                                       | Android version |
|-------------------------------------------------|-----------------|
| [twrp-3.7.1_12-vayu.img](https://github.com/woa-vayu/POCOX3Pro-Guides/releases/download/Recoveries/twrp-3.7.1_12-vayu.img) | Android 12/12.1/13/14 |
| [twrp-3.7.0_11-vayu.img](https://github.com/woa-vayu/POCOX3Pro-Guides/releases/download/Recoveries/twrp-3.7.0_11-vayu.img) | Android 11 |

- [Platform Tools from Google (ADB and Fastboot)](https://developer.android.com/studio/releases/platform-tools)
- A Windows PC

## Disclaimers

> [!WARNING]
> - If you see a warning and/or error during the process, it is not normal. Contact us on telegram if you see anything odd, but do not continue or proceed on your own, you will break things further.
> - Do not run all commands at once.

# Steps 🛠️

## Acquiring all files

<details>
    <summary>Here's how to acquire the Android SDK Platform Tools: <b>Click to expand</b></summary>
    <p>


First, start by going to the [Android Platform SDK download page](https://developer.android.com/studio/releases/platform-tools) on your computer.

![SDK-1-Top](https://github.com/WOA-Project/SurfaceDuo-Guides/assets/3755345/4c1c3762-24d8-4150-ac69-670738eb62c1)

Once on the page, scroll a little bit down til you see the link to download the platform tools for Windows.

![SDK-2-Mid](https://github.com/WOA-Project/SurfaceDuo-Guides/assets/3755345/cd14a232-4995-480f-a061-54507e83cf41)

Click on it, an EULA will open like below:

![SDK-3-EULA](https://github.com/WOA-Project/SurfaceDuo-Guides/assets/3755345/16d6b7df-ab56-414c-b1a5-561ec6b3ae4e)

Scroll all the way down (after reading it if that's your thing)

![SDK-4-EULA-Bottom](https://github.com/WOA-Project/SurfaceDuo-Guides/assets/3755345/1368b2b0-74b8-4a7c-9aff-df2ca25c2f42)

Tick "I have read and agree to above terms conditions"

![SDK-5-EULA-TICK (alt)](https://github.com/WOA-Project/SurfaceDuo-Guides/assets/3755345/02905fa2-64b8-426b-b42f-c1bb88eaa88a)

And click download

![SDK-5-EULA-TICK](https://github.com/WOA-Project/SurfaceDuo-Guides/assets/3755345/0983f27a-76e7-4fda-ac4d-adaa56702e90)

Save the file on your computer, and extract the zip file by opening it, and selecting extract all.

![SDK-6-DL](https://github.com/WOA-Project/SurfaceDuo-Guides/assets/3755345/adc1bba0-6118-418e-9005-e2db12860893)

  </p>
</details>

## Booting to TWRP

- Reboot your device into TWRP, assuming you have installed it previously

Your POCO X3 Pro will boot into TWRP.

## Entering Mass Storage Mode

- Run the mass storage shell script in order to boot into Mass Storage from TWRP. You must decrypt your data if it asks you to.

```batch
adb shell msc
```

- If it asks you to run it once again, do so

Your POCO X3 Pro should now be in USB Mass Storage Mode.

## Updating Drivers

> [!WARNING]
> From now on we will assume X: is the Windows partition for all commands. Replace them correctly with what you previously picked or you will lose data on your PC.

- Download the latest driver package from https://github.com/woa-vayu/POCOX3Pro-Releases/releases/latest

Note: Here's a table of what to download if you're a bit lost:

| File Name                                       | Target Device         |
|-------------------------------------------------|-----------------------|
| POCOX3Pro-Drivers-v2XXX.XX-Desktop.7z           | POCO X3 Pro           |

- Extract the driver package, and go to the folder where you extracted it.

- Double click the ```OfflineUpdater.cmd``` file.

- Accept the User Account Control warning when prompted

- If asked enter the drive letter of the connected phone in mass storage, as we previously mentioned, for us it's currently ```X:```, but it may very well be different for you. In our example, we enter ```X:``` and then press enter.

- The process may take a while, once it is done, you will be prompted to press any key, press enter when that's the case.

Congratulations, you just updated your drivers!

- You can now reboot your phone using:

```batch
adb reboot bootloader
```

You will be put into POCO X3 Pro's bootloader.

## Updating UEFI

Simply use the latest UEFI image

- Assuming you are in POCO X3 Pro's bootloader, run the following command to boot into Windows:

```batch
fastboot boot uefi.img
```

### For Dual Boot installations, follow the [Dual Boot](/InstallWindows-en/DualBoot.md) guide again.

---

_**© 2020-2024 The Duo WOA Authors**_
