# Teracube-device_minimum

Device tree for OMNI Android 9.0 TWRP build

Forked from [mrmazakblu's tree](https://github.com/mrmazakblu/Teracube_minimum_twrp-device-tree)

Built using [TWRP-device-tree-generator](https://github.com/SebaUbuntu/TWRP-device-tree-generator) with physical Teracube One for adb access during generation script

## Build instructions

1. Follow [these instructions](https://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni/tree/twrp-9.0#getting-started) to initialize a twrp directory for building TWRP. I linked the Android 9.0 branch since this is the device tree for the Android 9.0 build of TWRP.
2. Clone this repo to your `twrp/device/teracube/Teracube_One/` directory
3. Clone the [Teracube Kernel source](https://github.com/Teracube-Inc/kernel_teracube_one-4.4) to your `twrp/kernel/teracube/Teracube_One` directory
4. Save [this config](https://raw.githubusercontent.com/Teracube-Inc/kernel_teracube_one-4.4/teracube_one-p-oss/arch/arm64/configs/v7101o_defconfig) as `kernel/teracube/Teracube_One/arch/arm64/configs/Teracube_One_defconfig`
5. Run the following commands:
- `export ALLOW_MISSING_DEPENDENCIES=true`
- `. build/envsetup.sh`
- `lunch omni_Teracube_One-eng`
- `mka recoveryimage`
