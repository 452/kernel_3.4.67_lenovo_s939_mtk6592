Linux Kernel source code for Lenovo S930 Android Phone
==============

## Useful commands
```sh
head -n 53024 /dev/urandom > /dev/fb0
```

## Config

```sh
mediatek/config/stella/autoconfig/kconfig/project
```

## Build
```sh
export ARCH=arm
export SUBARCH=arm
export TARGET_PRODUCT=stella
export CROSS_COMPILE=arm-linux-androideabi-
export CC=arm-linux-androideabi-
./makeMtk stella n k
```

## Repack
you can download and unpack official stock image boot.img
or some from this site with already ported android http://www.needrom.com/category/lenovo/serial-s/s930
```sh
# https://github.com/bgcngm/mtk-tools
/data/git/mtk-tools/repack-MTK.pl -boot --debug '/data/kernels/android/repack/boot.img-kernel.img' /data/kernels/android/repack/boot.img-ramdisk /data/kernels/android/repack/newboot.img
```

## Flash
```sh
fastboot flash boot /data/kernels/android/repack/newboot.img; fastboot reboot
```
#### LCM (liquid crystal monitor, video display) for lenovo S930
```sh
# To choose LK LCM driver name
CUSTOM_LK_LCM=hx8394a_hd720_dsi_vdo_tianma nt35521_hd720_dsi_vdo_boe
# To choose kernel LCM driver name
CUSTOM_KERNEL_LCM=hx8394a_hd720_dsi_vdo_tianma nt35521_hd720_dsi_vdo_boe
# To choose uboot LCM driver name
CUSTOM_UBOOT_LCM=hx8394a_hd720_dsi_vdo_tianma nt35521_hd720_dsi_vdo_boe
```
#### LCM Modes
U:720x1280p-0

## ProjectConfig list
#### Boards
> mediatek/config/stella Lenovo S930 Smartphone

> mediatek/config/stellap Lenovo S939 Smartphone
```sh
find -name 'ProjectConfig.mk'
./mediatek/config/stellap/ProjectConfig.mk # Lenovo S939 Smartphone
./mediatek/config/common/ProjectConfig.mk
./mediatek/config/lenovo82_cwet_kk/ProjectConfig.mk
./mediatek/config/smarttp/ProjectConfig.mk
./mediatek/config/stella/ProjectConfig.mk # Lenovo S930 Smartphone
./mediatek/config/mt6592/ProjectConfig.mk
./mediatek/config/stellaptd/ProjectConfig.mk
./mediatek/config/lenovo92_cwet_kk/ProjectConfig.mk
./mediatek/config/sofina/ProjectConfig.mk
./mediatek/config/mt6582/ProjectConfig.mk
./mediatek/config/phaeton/ProjectConfig.mk
./mediatek/config/lenovo92_cwet_td/ProjectConfig.mk
./mediatek/config/scofield/ProjectConfig.mk
./mediatek/config/scofieldtd/ProjectConfig.mk
./mediatek/config/sofinatd/ProjectConfig.mk
./mediatek/config/banyan_addon_x86/ProjectConfig.mk
./mediatek/config/lenovo82_cwet_td/ProjectConfig.mk
./mediatek/config/sharp/ProjectConfig.mk
./mediatek/config/sharp/sharp/ProjectConfig.mk
```

#### Links
https://superuser.com/questions/860820/fbcon-use-android-msm-framebuffer-device-for-boot-console

http://moi.vonos.net/linux/framebuffer-drivers
