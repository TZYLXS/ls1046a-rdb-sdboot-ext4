# OpenWrt Firmware for NXP LS1046A-RDB

> 交流群：778213624/339426057/1063542188

OpenWrt SD card boot firmware with ext4 rootfs for the NXP Layerscape LS1046A-RDB board.

## Files

### layerscape target
| File | Description |
|------|-------------|
| `openwrt-layerscape-armv8_64b-fsl_ls1046a-rdb-sdboot-ext4-sdcard.img.gz` | SD card disk image (ext4 rootfs) |
| `openwrt-layerscape-armv8_64b-fsl_ls1046a-rdb-sdboot-ext4-sysupgrade.bin.gz` | Sysupgrade package |
| `openwrt-layerscape-armv8_64b-fsl_ls1046a-rdb-sdboot.manifest` | Installed package manifest |
| `openwrt-ls1046a-sha256sums.txt` | SHA256 checksums |

### nxpsoc target
| File | Description |
|------|-------------|
| `openwrt-nxpsoc-armv8_64b-fsl_ls1046a-rdb-sdboot-ext4-sdcard.img.gz` | SD card disk image (ext4 rootfs) |
| `openwrt-nxpsoc-armv8_64b-fsl_ls1046a-rdb-sdboot-ext4-sysupgrade.bin.gz` | Sysupgrade package |

## Kernel
Linux 5.10.271

## How to flash
1. Decompress the sdcard image: `gunzip openwrt-*-sdcard.img.gz`
2. Write to SD card: `dd if=openwrt-*-sdcard.img of=/dev/sdX bs=4M conv=fsync`
3. Boot the LS1046A-RDB from SD card
