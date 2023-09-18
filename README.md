# SkylineUI #

[![Download SkylineUI](https://img.shields.io/sourceforge/dt/skylineui.svg)](https://sourceforge.net/projects/skylineui/files/latest/download)

### Sync SkylineUI Source ###

```bash

# Initialize local repository

$ mkdir SkylineUI
$ cd SkylineUI
```

- Repo Init Source
```bash
$ repo init -u https://github.com/SkylineUI/manifest -b aosp-13
```

Once you have chosen a source branch, you can proceed with the synchronization using the following command:
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
$ mka bacon -j$(nproc --all)
```

# Credits:

| Project                           |
|-------------------------------|
| **Android Open Source Project**   |
| [**VoidUI**](https://github.com/VoidUI-Tiramisu) |
| [**PixelExperience**](https://github.com/PixelExperience) |
| [**EvolutionX**](https://github.com/Evolution-X) |
| [**LineageOS**](https://github.com/LineageOS) |
| [**crDroid**](https://github.com/crdroidandroid) |
| [**PixysOS**](https://github.com/PixysOS) |
| [**YAAP**](https://github.com/yaap) |

 * And too many other roms that I forgot to mention
