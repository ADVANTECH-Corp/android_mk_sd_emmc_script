# android_mk_sd_emmc_script
This is a shell script for create android sd card or emmc.

step1  Create the image and scripts folder
      ~$mkdir image
      ~$mkdir scripts

step2  In scripts, please download shell script in scripts folder.
      ~$cd scripts
      ~/scripts$ git clone https://github.com/ADVANTECH-Corp/android_mk_sd_emmc_script.git -b M6.0.1_2.1.0 

Step3  Copy the images and uboot to image folder.
       [boot.img, recovery.img ,system.img, u-boot_crc.bin, u-boot_crc.bin.crc, update.zip]
      ~$cd image
      ~/image$ copy boot.img recovery.img system.img u-boot_crc.bin u-boot_crc.bin.crc update.zip .

step4  Insert the SD card on your PC.
       Check SD card the partition number (example: /dev/sdb) 
       Run shell script
      ~$cd scripts
      ~/scripts$./mksd-andorid.sh /dev/sdb

