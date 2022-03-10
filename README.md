## Device Tree for the Samsung Galaxy S21 FE 5G (SM-G990B Snapdragon)
You will need to get the [TWRP Minimal Manifest](https://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp) files

## How-to compile:

```sh
export ALLOW_MISSING_DEPENDENCIES=true
. build/envsetup.sh
lunch twrp_r9q-eng
mka recoveryimage
```

## Install

```
Flash latest release && vbmeta-disabled with odin and disable auto-reboot
Reboot directly into recovery
Terminal -> type "multidisabler"
Format data, cache
enjoy
```

## Bugs

```
Touch not working
```

## Workaround untill it's resolved:

```
Boot into recovery
Connect the device to your pc
open termianl
adb shell
twrp format data
twrp wipe data
twrp wipe cache
twrp wipe dalvik
adb push /path/to/file /data
twrp install /data/file.zip
```

## notes

```
To flash gsi I used ChonDoe_Flasher.zip
```