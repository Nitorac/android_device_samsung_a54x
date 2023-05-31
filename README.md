# android_device_samsung_a54x
TWRP device tree for the Samsung A54 5G (Exynos)

Achieved by learning from @afaneh92 other TWRP device trees (big thanks for your work !)

## What's working ?
 - External SD
 - MTP (none of internal data since no encryption disabler is working)
 - Backup only of some partitions (I haven't tested to restore them)

## What's not working ?
 - Main partitions read-write
 - Restore partitions (please don't try, you could hard brick / loose your phone if you try to do so !)

## What's missing ?
 - A custom patched vbmeta.img that could be installed through Odin without a boot issue
 - Multidisabler and encryption disabler (maybe the generic ones could work after I fix the partition issues)

## How to install
 - The only way I achieved to install it is by flashing the img through the TWRP app with a Magisk rooted stock rom 

## How to compile
With a proper toolchain:

```bash
export ALLOW_MISSING_DEPENDENCIES=true
. build/envsetup.sh
lunch twrp_a54x-eng
make recoveryimage
```
