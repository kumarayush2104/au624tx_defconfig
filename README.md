# au624tx_defconfig

<b> How to use :-</b>

1. Navigate to kernel source home folder ( Where you see folders like arch, blocks,certs ) <code> cd /path/to/kernel/folder</code> <br>
2. Clear the kernel sources <code>make mrproper</code>
3. Clone the repo <code>git clone git://github.com/kumarayush2104/au624tx_defconfig ~/defconfig;mv ~/defconfig/ .config;rm -rf ~/defconfig</code>
4. Start the kernel build <code>make -j5</code> and install it <code>sudo make install;sudo make modules_install</code> <br> 

## What are the the things enabled in this config
<b> Devices </b>
1. Synaptics touchpad/Libinput, keyboard,mouse (Input devices)
2. iwlwifi, rt8169 (Network Drivers)
3. i915 and nouveau (Display Drivers)
4. USB, DVD and Realtek card reader Drivers 

<b> File systems </b> <br>
ext4, ext3, f2fs, ntfs, fat, exfat, udf, iso, loop, mmc, lvm

<b> Misc Devices </b><br>
EFI stuffs, Accelerometer, Intel Mei, Thermal, Sensors, and all types of acpi stuffs required by this model

<b> Compression </b><br>
This kernel uses XZ compression

## Want to add something in kernel ?? <br>
Edit the config <code>nano .config</code> or run menuconfig <code> make menuconfig </code> (I assume you are in kernel home directory)

## WARNING WARNING WARNING !!!
<b> STUFFS OTHER THAN MENTIONED ABOVE ARE DISABLED </b> <br>
<b> **TESTED ON GENTOO LINUX** </b>
