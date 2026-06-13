# DryBloodOS

## Getting Started
This project contains work of [GrapheneOS](https://github.com/GrapheneOS) and [AxionOS](https://github.com/AxionAOSP) developers team as well as [AOSP](https://source.android.com) source code.

## Download And Sync The Source
- create and enter directory:
``` bash
mkdir DryBloodOS && cd DryBloodOS
```
- init the manifest:
```bash
repo init -u https://github.com/DryBlood-Project/platform_manifest.git -b 2026060600-2.7
```
- fast sync:
```bash
repo sync -c --force-sync --optimized-fetch --no-tags --no-clone-bundle --prune -j$(nproc --all)
```
- normal sync:
```bash
repo -j$(nproc --all)
```

# About "dbuild" tool
- Use "." or "source" to run dbuild directly in your terminal to prevent lunching every time you use dbuild.
- On every first use dbuild will ask you what is your device codename you want to work with or you can export it yourself by:
```bash
export DEVICE_CODENAME="your device code name"
```
- To get help use:
```bash
. dbuild help
```
# Building
- if you're not already in bash enviroment which is required for dbuild to work use:
```
bash
```
- to pull device trees for your device:
```bash
. dbuild pull
```
- to start build process:
```bash
. dbuild build
```

Other things later (signing, making ota etc)