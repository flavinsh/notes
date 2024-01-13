---
tags:
  - Android
---
## Clean flash
When install a custom ROM on an [[Android]] device, a **clean flash** requires to format all data in the phone's storage, including:
- system data
- cached files
- Dalvik cache
- internal storage

## Dirty flash
A **dirty flash** refers to an [[OTA]] update or upgrading an old ROM to a newer version without having to factory reset or wipe your device.

> [!comment] Dirty flash a ROM is **not** recommended, as it can cause all kinds of random problems. 

# Step to install a custom ROM

### Prepare computer
1. Download [Platform Tools](https://developer.android.com/tools/releases/platform-tools) on your computer and store the `platform-tools`in your home directory.
2. Download the [TWRP recovery image](https://twrp.me/Devices/) for your specific device, rename it `twrp.zip` and place it in the `platform-tools` folder.
4. Download a custom ROM, rename it `rom.zip`and place it in the `platform-tools`folder.
5. Download a boot image that is suitable for your phone, rename it `boot.img` and place it in the `platform-tools`folder.
6. Open Terminal and `cd` to the `platform-tools` folder.

### Prepare Android device
1. Go to Settings > About > Build number > tap multiple times to enable Developper mode.
2. Go to Settings > System > Developper options > Enable USB debugging .
3. Connect the Android device with the computer using an USB cable.

### Install custom ROM
1. Run `./adb reboot bootloader` to restart in bootloader mode.
2. Run `./fastboot boot twrp.img` to launch TWRP recovery.
3. In TWRP, click Wipe > Format Data
4. In TRWP click Wipe > Advanced Wipe > Dalvik cache / System / Cache
5. In TWRP click: Advanced > ADB Sideload
6. Run `./adb sideload rom.zip`
7. Reboot

Alternatively, you can transfer `rom.zip`to the Android device and in TWRP, click Install > Select Storage > MicroSD and select `rom.zip`

### Install boot image
2. Run `./adb devices` and `./fastboot devices` to check if the Android device has been detected
3. Run  `fastboot flash boot boot.img`
4. Run `./fastboot reboot` to restart your device

