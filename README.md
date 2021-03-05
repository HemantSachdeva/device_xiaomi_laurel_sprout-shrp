
# SHRP Device Tree for Mi A3 (laurel_sprout)

The Mi A3 (codenamed "laurel_sprout") is a mid-range smartphone from Xiaomi. It was announced and released in July 2019.

## Device specifications

| Feature                 | Specification                                                   |
| :---------------------- | :---------------------------------------------------------------|
| Chipset                 | Qualcomm SM6125 Snapdragon 665 (11 nm)                          |
| CPU                     | Octa-core (4x2.0 GHz Kryo 260 Gold & 4x1.8 GHz Kryo 260 Silver) |
| GPU                     | Adreno 610                                                      |
| Memory                  | 4/6 GB                                                          |
| Shipped Android Version | 9.0                                                             |
| Storage                 | 64/128 GB UFS 2.1                                               |
| SIM                     | Hybrid Dual SIM (Nano-SIM, dual stand-by)                       |
| MicroSD                 | Up to 256 GB                                                    |
| Battery                 | 4030 mAh Li-Po (non-removable)                                  |
| Dimensions              | 153.5 x 71.9 x 8.5 mm                                           |
| Display                 | 6.09 inch, 720 x 1560 (19.5:9 ratio)                            |
| Rear Camera 1           | 48 MP, f/1.8, 26mm (wide), 1/2.0", 0.8µm, PDAF                  |
| Rear Camera 2           | 8 MP, f/2.2, 13mm (ultrawide), 1/4.0", 1.12µm                   |
| Rear Camera 3           | 2 MP, f/2.4, (depth)                                            |
| Front Camera            | 32 MP, f/2.0, 26mm (wide), 1/2.8", 0.8µm                        |
| Fingerprint             | Under display, optical                                          |
| Sensors                 | Accelerometer, Gyro, Proximity, Compass                         |

## Device picture

![Mi A3](http://i01.appmifile.com/webfile/globalimg/products/pc/mi-a3/specs2.png)

## Kernel source 
Available at https://github.com/HemantSachdeva/kernel_xiaomi_laurel_sprout

## How to build
1. Set up the build environment by following intructions from [here](https://shrp.github.io/#/guide?id=build-shrp)
2. In the root folder of cloned synced shrp source clone the device tree:
```
git clone -b android-9.0 https://github.com/SHRP-Devices/device_xiaomi_laurel_sprout.git device/xiaomi/laurel_sprout
```
3. To build:
```
. build/envsetup.sh && lunch omni_laurel_sprout-eng && mka recoveryimage -j128
```

## Note
All the scripts are written in according to bash format so consider using bash shell while building.
You can switch to bash shell just by typing ```bash``` command and logout from it by ```exit``` after you complete the build.

Source uses ```python2``` and it may give you some syntax error for if you have ```python3```. So install python2 and use following command to activate ```python2``` for building: 
```
virtualenv -p /usr/bin/python2 xyz && source xyz/bin/activate
```
You need virtualenv package to be installed. (Tested on Ubuntu, use virtualenv2 in arch based linux distros.)