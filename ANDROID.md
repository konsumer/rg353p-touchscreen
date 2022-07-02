# Android

The first step for figuring out the linux touchscreen driver for RG353P was loading android and inspecting the system.

We already have root (type `su` in `adb shell`) but magisk can make it easier to install other tools, so it's optional, but will make things easier.

## magisk

[This](https://www.youtube.com/watch?v=84LG5eBunyw) has really good complete instructions for magisk + playstore. I did it it a bit more streamlined, but you can use that if it doesn't work.

- Install github release of Magisk APK on RG353P
- Install System info APK on RG353P
- open Magisk on RG353P, choose "install" and "direct install"
- install magisk gapps


## info

- Tap on "Build number" in settings 5 times to enable developer-mode, turn on USB debugging, plug your device into your computer with USB.

```
# should show your device
adb devices

# enable root-mode
adb root

# kernel config
adb pull /proc/config.gz .

# list device-info
adb shell ls -l /sys/module
```
