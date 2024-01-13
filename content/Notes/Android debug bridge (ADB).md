---
tags:
  - Android
---
**Android debug bridge** (ADB) is a command-line tool that lets you communicate between a computer and an [[Android]] device. The `adb` command facilitates a variety of device actions, such as installing and debugging apps.

## ADB commands

Install [Platform Tools](https://developer.android.com/tools/releases/platform-tools)  somewhere on your computer and then `cd`to the `platform-tools` folder and run the following commands:

| Command                                      | Description                                                          |
| -------------------------------------------- | -------------------------------------------------------------------- |
| `add connect xxx.xxx.x.xx`                   | Connect with wireless ADB using IP address of device                 |
| `adb devices`                                | Check if a device is connected with USB                              |
| `adb install app.apk`                        | Install apk file located in the `platform-tools`folder to the device |
| `adb sideload rom.zip`                       | Flash ROM located in the 'platform-tools' folder                     |
| `adb reboot`                                 | Reboot device normally                                               |
| `adb reboot recovery`                        | Reboot device in recovery mode                                       |
| `adb reboot-bootloader`                      | Reboot device in bootloader mode                                     |
| `adb shell [command]`                        | Execute command                                                      |
| `adb shell getprop ro.build.version.release` | Check Android version                                                                     |

