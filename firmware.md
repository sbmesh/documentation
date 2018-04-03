# Firmware Cooking

To be used with the [lime-sdk](https://github.com/libremesh/lime-sdk) firmware cooker.

Currently supported devices:
- Ubiquiti NanoStation M5 (XW)


## Build Instructions

### Requirements

- NanoStation M5 (XW) w/ airOS downgraded to v5.5.10
- VM or build environment similar to the [Vagrantfile](https://github.com/sbmesh/documentation/Vagrantfile) in this repo


### Preparing the environment

```
git clone https://github.com/libremesh/lime-sdk.git
cd lime-sdk
umask 022
```
**Note:** Running `umask 022` might only be necessary in our particular Vagrant box

### Cook the firmware

```
./cooker -c ar71xx/generic --profile=ubnt-nano-m-xw --flavor=lime_default --community=sbmesh/common --remote
```

Images will be in `output/`.

The image suffixed with `factory` is for fresh installations of LibreMesh from AirOS, and `sysupgrade` is for upgrading an existing LibreMesh build.

## Flash Instructions

[Guide for flashing the NanoStation M5](https://github.com/sbmesh/documentation/flashing.md)
