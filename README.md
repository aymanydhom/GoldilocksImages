# GoldilocksImages
 Linux images for Future Electronics Goldilocks kit

Mama Bear Re-Programming Mama Bear Board is preprogrammed with latest firmware. In case of software update or in need of reprograming the Mama Bear eMMC, the following steps should be followed:

1. Download "uuu" NXP upgrading tool from https://github.com/NXPmicro/mfgtools/releases
2. Download uboot and Linux image files from the repo and put in the same folder as uuu
3. Open CMD window from this folder (if using windows, make sure to use "Run As Administrato").
4. Power on Mama Bear
5. Connect USB cable between computer and Mama Bear USB Programming Port (J13)
6. In console window, hit enter key, it should stop in uboot
7. Type “fastboot 0”, should hear USB enumerating sound on the computer
8. In CMD window, type “ uuu -b emmc_all imx-boot goldilocks-image-q10.zst” (please use the image file name on your computer), and hit enter key
9. In CMD window, the progress of programming should be shown, wait until “Done”. Normally it takes about 10~15 minutes
10. Power cycle Mama Bear, wait until boot up complete
11. Login with “root”, no password needed
12. Type command “ shutdown now”, wait until the last message “reboot: Power down” shows up, then disconnect power
