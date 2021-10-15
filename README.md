### Requirements
- Around 100G disk space.
- A computer with at least 16GB RAM running Linux (recommended) or MacOS.
- Build environment [setup](https://github.com/akhilnarang/scripts).

### Instructions

```
repo init -u https://github.com/BubbleGumOS/android_manifest -b bubblegum-12
```

```
 repo sync -c --force-sync --optimized-fetch --no-tags --no-clone-bundle --prune -j$(nproc --all)
```

```
   source build/envsetup.sh
   lunch bubblegum_<devicecodename>-userdebug
   make bacon -j$(nproc --all)
```