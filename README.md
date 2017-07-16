# dji_system.bin
DJI is currently in violation of GPL... these binaries are intended to be distributed to end users that have purchased either an inspire2, Mavic, Spark, or P4 variant drone,and are seeking to downgrade their aircraft back to its factory state. 

https://www.gnu.org/licenses/gpl-faq.en.html
“GPL gives a person permission to make & redistribute copies of the program if & when that person chooses to do so”
https://www.gnu.org/licenses/gpl-faq.en.html#CanIDemandACopy
“You can charge people a fee to get a copy from you. You can't require people to pay you when they get a copy from someone else.”

“if someone pays your fee and gets a copy, the GPL gives them the freedom to release it to the public, with or without a fee”
“The GPL says that anyone who receives a copy from you has the right to redistribute copies, modified or not.”
https://www.gnu.org/licenses/gpl-faq.en.html#DoesTheGPLAllowNDA
“If it depends on a nonfree library to run at all, it cannot be part of a free operating system such as GNU;”
https://www.gnu.org/licenses/gpl-faq.en.html#FSWithNFLibs
“If they form a single combined program then the main program must be released under the GPL”
You cannot incorporate GPL-covered software in a proprietary system.”
https://www.gnu.org/licenses/gpl-faq.en.html#GPLInProprietarySystem
“you must make sure that the free and nonfree programs communicate at arms length”
https://www.gnu.org/licenses/gpl-faq.en.html#GPLInProprietarySystem
“Can I release a modified version of a GPL-covered program in binary form only?”
https://www.gnu.org/licenses/gpl-faq.en.html#ModifiedJustBinary
“The exception for the case where you received a written offer for source code is quite limited.”
“must be open to everyone who has a copy”
“This is a well-meaning request, but this method of providing the source doesn't really do the job.”
https://www.gnu.org/licenses/gpl-faq.en.html#DistributingSourceIsInconvenient
“As long as you make the source and binaries available so that the users can see what's available and take what they want”
“Complete corresponding source means the source that the binaries were made from”
https://www.gnu.org/licenses/gpl-faq.en.html#MustSourceBuildToMatchExactHashOfBinary
“If the version has been released elsewhere, then the thief probably does have the right to make copies and redistribute them under the GPL”
https://www.gnu.org/licenses/gpl-faq.en.html#TradeSecretRelease
“If a company distributes a copy to you and claims it is a trade secret, the company has violated the GPL” 
https://www.gnu.org/licenses/gpl-faq.en.html#TradeSecretRelease


Please contact FSF and ask for the GPL source code that DJI uses to be published. 
[![Fuck yeah](https://media.giphy.com/media/wi8Ez1mwRcKGI/giphy.gif)](https://www.youtube.com/watch?v=T437DdmFNPU)

http://www.fsf.org/licensing/compliance

Known Md5s of files pulled from DJI updates, user contributed files, and exploits. 
```
MD5 (UniversalFireworksTar_dji_system.bin) = 10e4b4ba3da6e2e2455f2958ea897e9c
MD5 (V01.00.0300_Spark_dji_system.bin) = bf81af1c10318e8549bb78b0fef85013
MD5 (V01.00.0400_Spark_dji_system.bin) = 65f15f4cbe7d761459c7a09ebc660801
MD5 (V01.03.0400_Mavic_dji_system.bin) = a5ac037462b4f902bfa6cb8d9fe395ae
MD5 (V01.03.0700_Mavic_dji_system.bin) = 891904fad23add85e8c50a7902f272df
MD5 (V01.03.0800_Mavic_dji_system.bin) = 6602c26ed0729581246853d7c988a4ae
MD5 (V01.03.0900_Mavic_dji_system.bin) = 984446beb028443670091e07d3bbd752
MD5 (V1.02.0602_P4crafted.dji_system.bin) = 36e11566ae6e303ec5c407f9c0f6c382
MD5 (V2.00.0106_P4crafted.dji_system.bin) = a49944bb254354ec064bee13c491fa1e
```

Known files from *homebrew* variants

MD5 (mavic_combined_400_root.bin) = 86b322026612e96fa09373bc8560674a - from hostile (drops root & downgrades to Mavic .400)

To combine your own files do the following (using gnu-tar from brew if on OSX):
```
$ cp UniversalFireworksTar_dji_system.bin mavic_combined_700_root.bin 
$ gtar --concatenate --file mavic_combined_700_root.tar V01.03.0700_Mavic_dji_system.bin
$ tar tvf mavic_combined_700_root.tar 
sh-3.2# mv mavic_combined_700_root.tar mavic_combined_700_root.bin

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
```
You can see this file has BOTH the root, and the downgrade packaged together. 

This is the most up to date source of info on "rooting" DJI aircraft. Start here with questions
http://dji.retroroms.info 

