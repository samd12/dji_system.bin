# dji_system.bin
DJI is currently in violation of GPL... these binaries are intended to be distributed to end users that have purchased either an inspire2, Mavic, Spark, or P4 variant drone,and are seeking to downgrade their aircraft back to its factory state. 

Please contact FSF and ask for the GPL source code that DJI uses to be published. 

http://www.fsf.org/licensing/compliance

Known Md5s of files pulled from DJI updates. 
MD5 (V01.00.0300_Spark_dji_system.bin) = bf81af1c10318e8549bb78b0fef85013
MD5 (V01.00.0400_Spark_dji_system.bin) = 65f15f4cbe7d761459c7a09ebc660801
MD5 (V01.03.0400_Mavic_dji_system.bin) = a5ac037462b4f902bfa6cb8d9fe395ae
MD5 (V01.03.0700_Mavic_dji_system.bin) = 891904fad23add85e8c50a7902f272df
MD5 (V01.03.0800_Mavic_dji_system.bin) = 6602c26ed0729581246853d7c988a4ae
MD5 (V01.03.0900_Mavic_dji_system.bin) = 984446beb028443670091e07d3bbd752

Known files from *homebrew* variants

MD5 (V01.00.0X00_XXXX_dji_system.bin)  = TBDTBDTBDTBDTBDTBDTBDTBDTBDTBDTBD

Instructions thanks to vk2fro for taking the initiative to start *doing* instead of asking "Where is the FAQ?" like so many others

```
To flash, choose a firmware and rename it dji_system.bin. Copy it to the pyduml folder.

cd to /dev with the mavic connected and find the usb modem (in my case, tty.usbmodem14E5).

execute python pyduml.py /dev/<your.modem.number> (tty.usbmodem14E5).

Flashing takes around 10 minutes. Watch the lights on the mavic.

To root, rename fireworks.tar dji_system.bin and re run the script as above. Power cycle the drone 2 minutes after running the script. DO NOT TURN OFF YET after the power cycle.

Now adb devices, and you should see the mavic listed. (RedHerring has Fangs!). adb shell into it and execute these two lines (use copy and paste, a typo = a brick!) in the shell:

mount -o remount,rw /system
echo /system/bin/adb_en.sh >> /system/bin/start_dji_system.sh
reboot

This makes the root permenant.
```

