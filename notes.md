## 2018.7.19 Magisk v16.7
(XDA Post: [here](https://forum.xda-developers.com/showpost.php?p=77108384&postcount=44))

A stable release is imminent!

### Hot Fix (versionCode: 1671)
- Fix booting to fastboot on half-treble devices (OP5/5T on stable OOS, maybe more)
- Detect ramdisk partition for Huawei

### Bug Fixes
EMUI's logcat for some reason will change the permission of its output file, and since Magisk will do several logcat commands dumping output to `/dev/null`, the permission is messed up, causing tons of stuff to break, including `adbd`; the issue is now fixed. Some new Treble devices (e.g. OnePlus 5/5T) had some issues with the "lazy" method I used to early mount partitions, so the "proper" way is introduced:  `magiskinit` will start reading fstab in device trees to detect the partition partname. A positive side effect is that some custom Treble devices (many Xiaomi devices) modifies the device tree to redirect vendor to an unused partition, and this is now fully supported!

### Legacy Support
Starting from v16.7, the native part of Magisk is compiled against SDK 16 (Android 4.1 JellyBean), which is the beginning of legacy support. This doesn't mean you can flash Magisk on your obsolete devices now, as there are tons of stuffs needed to be done: Magisk Manager does not install on anything lower than Android 5.0; most features are not even tested yet. Proper legacy support won't happen until the next release is pushed to the stable channel though, v17 is my top priority now and I want it to be as bug free as possible!

### Full Changelog: [here](https://forum.xda-developers.com/showpost.php?p=68966755&postcount=2)
