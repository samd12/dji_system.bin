# dji_system.bin
If you have access to this, do NOT link it outside of slack, in videos, readme's, FAQs, etc

DJI is currently in violation of GPL... these binaries are intended to be distributed to end users that have purchased either an inspire2, Mavic, Spark, or P4 variant drone,and are seeking to downgrade their aircraft back to its factory state. 

Please contact FSF and ask for the GPL source code that DJI uses to be published. 

http://www.fsf.org/licensing/compliance

Known Md5s of files pulled from DJI updates, user contributed files, and exploits. 
MD5 (V01.00.0300_Spark_dji_system.bin) = bf81af1c10318e8549bb78b0fef85013
MD5 (V01.00.0400_Spark_dji_system.bin) = 65f15f4cbe7d761459c7a09ebc660801
MD5 (V01.03.0400_Mavic_dji_system.bin) = a5ac037462b4f902bfa6cb8d9fe395ae
MD5 (V01.03.0700_Mavic_dji_system.bin) = 891904fad23add85e8c50a7902f272df
MD5 (V01.03.0800_Mavic_dji_system.bin) = 6602c26ed0729581246853d7c988a4ae
MD5 (V01.03.0900_Mavic_dji_system.bin) = 984446beb028443670091e07d3bbd752
MD5 (V1.02.0602_P4crafted.dji_system.bin) = 36e11566ae6e303ec5c407f9c0f6c382
MD5 (V2.00.0106_P4crafted.dji_system.bin) = a49944bb254354ec064bee13c491fa1e
MD5 (UniversalFireworksTar_dji_system.bin) = 10e4b4ba3da6e2e2455f2958ea897e9c
MD5 (mavic_combined_700_root.bin) = 3613a4f0112cafbf04c7fc6d55e35295

Known files from *homebrew* variants

MD5 (V01.00.0X00_XXXX_dji_system.bin)  = TBDTBDTBDTBDTBDTBDTBDTBDTBDTBDTBD


To combine your own files do the following (using gnu-tar from brew if on OSX):
$ cp UniversalFireworksTar_dji_system.bin mavic_combined_700_root.bin 
$ gtar --concatenate --file mavic_combined_700_root.tar V01.03.0700_Mavic_dji_system.bin
$ tar tvf mavic_combined_700_root.tar 
-rw-r--r--  0 root   staff      37 Jul  9 01:51 Burning0day.txt
lrwxr-xr-x  0 root   staff       0 Jul  9 01:51 symlink -> /data/.bin
-rwxr-xr-x  0 root   staff     517 Jul  9 01:51 symlink/grep
-rwxrwxrwx  0 0      users   55072 Jul 12 15:41 wm220_0305_v34.04.00.23_20161122.pro.fw.sig
-rwxrwxrwx  0 0      users 1537056 Jul 12 15:41 wm220_0306_v03.02.30.13_20170405.pro.fw.sig
-rwxrwxrwx  0 0      users   20768 Jul 12 15:41 wm220_1200_v01.09.00.00_20161204.pro.fw.sig
-rwxrwxrwx  0 0      users   20768 Jul 12 15:41 wm220_1201_v01.09.00.00_20161204.pro.fw.sig
-rwxrwxrwx  0 0      users   20768 Jul 12 15:41 wm220_1202_v01.09.00.00_20161204.pro.fw.sig
-rwxrwxrwx  0 0      users   20768 Jul 12 15:41 wm220_1203_v01.09.00.00_20161204.pro.fw.sig
-rwxrwxrwx  0 0      users   28416 Jul 12 15:41 wm220_1100_v01.00.07.24_20161206.pro.fw.sig
-rwxrwxrwx  0 0      users   43488 Jul 12 15:41 wm220_0803_v00.00.04.08_20170314.pro.fw.sig
-rwxrwxrwx  0 0      users 15180832 Jul 12 15:41 wm220_0100_v02.02.56.29_20170317.pro.fw.sig
-rwxrwxrwx  0 0      users 37489024 Jul 12 15:41 wm220_0100_v02.06.04.84_20170324_ca02.pro.fw.sig
-rwxrwxrwx  0 0      users    60128 Jul 12 15:41 wm220_0101_v02.06.04.84_20170324_ca02.pro.fw.sig
-rwxrwxrwx  0 0      users   196544 Jul 12 15:41 wm220_0101_v02.02.56.29_20170317.pro.fw.sig
-rwxrwxrwx  0 0      users    91584 Jul 12 15:41 wm220_0400_v01.50.12.01_20170414.pro.fw.sig
-rwxrwxrwx  0 0      users    26432 Jul 12 15:41 wm220_0804_v01.00.00.08_20170113.pro.fw.sig
-rwxrwxrwx  0 0      users  4142592 Jul 12 15:41 wm220_0907_v47.26.02.11_20170419.pro.fw.sig
-rwxrwxrwx  0 0      users 41515328 Jul 12 15:41 wm220_0801_v01.05.00.20_20170331.pro.fw.sig
-rwxrwxrwx  0 0      users  5320416 Jul 12 15:41 wm220_0802_v01.00.03.08_20170116.pro.fw.sig
-rwxrwxrwx  0 0      users  3052000 Jul 12 15:41 wm220_0805_v01.01.00.87_20170427.pro.fw.sig
-rwxrwxrwx  0 0      users    92096 Jul 12 15:41 wm220_0905_v00.00.01.04_20170301.pro.fw.sig
-rwxrwxrwx  0 0      users     5888 Jul 12 15:41 wm220.cfg.sig

You can see this file has BOTH the root, and the downgrade packaged together. 

Instructions thanks to vk2fro for taking the initiative to start *doing* instead of asking "Where is the FAQ?" like so many others

```
Mavic Flashing Faq V0.3 by vk2fro
Flashing the Mavic Pro Drone is bloody simple with the pyduml.py script. You will need:
a linux or mac box (live usb will work for linux)
a mavic pro drone and connecting cable
the script (pyduml.py) - https://github.com/hdnes/pyduml
(mac only) homebrew - to install stuff
pip
python
libusb
adb (if you would like root)
a firmware file (check #archived_fw_flashing for my links (vk2fro) or grab them off your momsʼs git (this one if your reading from there).
a half hour and a coffee/beer

To flash, drag the firmware into the pyduml.py folder

open up a terminal and cd to /dev with the mavic connected and type ls tty.usb* and youʼll find the usb modem (in my case, tty.usbmodem14E5).

now cd back to the pyduml folder - if its in you home directory, cd ~/pyduml (donʼt forget the ~)

type mv <firmware name> dji_system.bin (this changes the name to work with the script)

execute python pyduml.py /dev/<your.modem.number> (tty.usbmodem14E5). 

python pyduml.py /dev/tty.usbmodem14E5 for example

Flashing takes around 10 minutes. Watch the lights on the mavic. The mavic will chime close to completion and when the lights stop flashing it is done. Be patient - 10 minutes seems like an awfully long time, but you donʼt get a progress bar like when you flash with assistant. Do not disconnect the drone when the script says its finished - thats only the upload portion!

To root, rename fireworks.tar dji_system.bin and re run the script as above. Power cycle the drone 2 minutes after running the script. DO NOT TURN OFF YET after the power cycle.

Now adb devices, and you should see the mavic listed. (RedHerring has Fangs!). adb shell into it and execute these two lines (use copy and paste, a typo = a brick!) in the shell:

mount -o remount,rw /system
echo /system/bin/adb_en.sh >> /system/bin/start_dji_system.sh
reboot

This makes the root permenant.

```

