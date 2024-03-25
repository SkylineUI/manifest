![SkylineUI](https://github.com/SkylineUI/manifest/raw/aosp-14/SkylineUIBanner.png)

# Manifest SkylineUI #

### Sync SkylineUI Source ###

```bash

# Initialize local repository

$ mkdir SkylineUI
$ cd SkylineUI
```

- Repo Init Source
```bash
$ repo init -u https://github.com/SkylineUI/manifest -b aosp-14
```

Now we proceed with the synchronization of the source with the following command:
```bash
$ repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```
**Note:** To save space and reduce download time during the synchronization process, you can also pass `--depth 1` to the `repo sync` command. However, using `--depth 1` will result in the repositories being synced without any commit history.

### Build ###

```bash

# Set up environment
$ . build/envsetup.sh

# Choose a target
$ lunch aosp_$device-userdebug

# Build the code
$ make bacon -j$(nproc --all)
```

# Build Flags
It will be your decision and if the device supports it `activate/deactivate` any of the following flags

`You must add these flags in aosp_$device.mk`

| Flag                          |
|-------------------------------|
TARGET_BOOT_ANIMATION_RES := 1080 |
TARGET_FACE_UNLOCK_SUPPORTED := true |
TARGET_CALL_RECORDING_SUPPORTED := true |
TARGET_BUILD_APERTURE := true |
TARGET_USES_MIUI_CAMERA := false |
TARGET_INCLUDES_MIUI_CAMERA := false |

# Credits:

| Projects                      |
|-------------------------------|
| **Android Open Source Project** |
| [**PixelOS**](https://github.com/PixelOS-AOSP) |
| [**PixelExperience**](https://github.com/PixelExperience) |
| [**EvolutionX**](https://github.com/Evolution-X) |
| [**LineageOS**](https://github.com/LineageOS) |
| [**DerpFest**](https://github.com/DerpFest-AOSP) |
| [**crDroid**](https://github.com/crdroidandroid) |
| [**PixysOS**](https://github.com/PixysOS) |
| [**YAAP**](https://github.com/yaap) |
