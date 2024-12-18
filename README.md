# Android device tree for samsung SM-S711U (r11q)

# How-to compile it:

## twrp-14 Manifest
    repo init --depth=1 -u https://github.com/MrFluffyOven/platform_manifest_twrp_aosp.git -b twrp-14
## Sync
    repo sync
## Clone TheNoobDevs Recovery Project TWRP tree
    git clone https://github.com/TNDRP/android_device_samsung_r11q.git -b android-14 device/samsung/r11q
## Prepare
    export ALLOW_MISSING_DEPENDENCIES=true; . build/envsetup.sh; lunch twrp_r11q-eng
## Repopick Patches
    repopick -Q "branch:android-14+status:open+-change:7371+-change:7543+-change:7553+-change:7671+-change:7717+-change:7718"
## Run the Build Command
    mka recoveryimage
