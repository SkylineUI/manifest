# SkylineUI #

### Sync ###

```bash

# Initialize local repository

$ mkdir SkylineUI
$ cd SkylineUI
$ repo init -u https://github.com/SkylineUI/manifest -b aosp-13

# Sync
$ repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

### Build ###

```bash

# Set up environment
$ . build/envsetup.sh

# Choose a target
$ lunch aosp_$device-userdebug

# Build the code
$ mka bacon -j$(nproc -all)
```

# Credits:

 * **Android Open Source Project**
 * [**VoidUI**](https://github.com/VoidUI-Tiramisu)
 * [**PixelExperience**](https://github.com/PixelExperience)
 * [**EvolutionX**](https://github.com/Evolution-X)
 * [**LineageOS**](https://github.com/LineageOS)
 * [**crDroid**](https://github.com/crdroidandroid)
 * [**PixysOS**](https://github.com/PixysOS)
 * [**YAAP**](https://github.com/yaap)

 * And too many other roms that I forgot to mention
