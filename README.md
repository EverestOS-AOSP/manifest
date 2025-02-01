# EverestOS

## Build Process

### Install ###

```bash

sudo apt install -y jq
```

### Initialize local repository
```
repo init -u https://github.com/EverestOS-AOSP/manifest -b exp --git-lfs
```
### Sync
```
repo sync -c --force-sync --optimized-fetch --no-tags --no-clone-bundle --prune -j$(nproc --all)
```

### Build ###

```
. build/envsetup.sh
```
```
lunch lineage_$device-ap4a-$build_type
```
```
make everest -j$(nproc --all)
```

## Devices

- [EverestOS-Devices](https://github.com/orgs/ProjectEverest-Devices/repositories)
