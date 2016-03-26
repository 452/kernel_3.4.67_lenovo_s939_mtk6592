Linux Kernel source code for Lenovo S930 Android Phone
==============

Build
```sh
export ARCH=arm
export SUBARCH=arm
export TARGET_PRODUCT=stella
export CROSS_COMPILE=arm-linux-androideabi-
export CC=arm-linux-androideabi-
./makeMtk stella n k
```

repack
```sh
# https://github.com/bgcngm/mtk-tools
/data/git/mtk-tools/repack-MTK.pl -boot --debug '/data/kernels/android/repack/boot.img-kernel.img' /data/kernels/android/repack/boot.img-ramdisk /data/kernels/android/repack/newboot.img
```

flash
```sh
fastboot flash boot /data/kernels/android/repack/newboot.img; fastboot reboot
```

ProjectConfig list
```sh
find -name 'ProjectConfig.mk'
./mediatek/config/stellap/ProjectConfig.mk
./mediatek/config/common/ProjectConfig.mk
./mediatek/config/lenovo82_cwet_kk/ProjectConfig.mk
./mediatek/config/smarttp/ProjectConfig.mk
./mediatek/config/stella/ProjectConfig.mk
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
