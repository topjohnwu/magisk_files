## 2018.9.1 Magisk v17.1
(XDA Post: [here](https://forum.xda-developers.com/showpost.php?p=77496559&postcount=45))

This long awaited stable release is delayed due to me moving to the US and some unexpected issues in the meantime. But hey it's here guys!  
I suggest those who care (e.g. module developers) follow me on [Twitter](https://twitter.com/topjohnwu), as I do most of the announcements other than Magisk releases over there.

### Hotfix v17.1
There was some incompatibility issues when upgrading from v16.0 to v17.0. If you are caught in a bootloop, first use the uninstaller to completely remove Magisk, then flash v17.1, I'm extremely sorry for all stuck in bootloops.

### Release Cycles
Starting from v17.0, the stable channel and the beta channel are considered as "public releases", meaning both will be well tested before release and should be good for most normal users as daily driver. In general (meaning no catastrophic bugs), each major version bump (e.g. `v17` -> `v18`) will be on the stable channel, and each minor version bump (e.g. `v17.0` -> `v17.1`) will be on the beta channel. For version codes, the first 3 digits represent the version of a public release (e.g. `17500` will be `v17.5`), the last 2 digits are for internal iterations (e.g. `17521` will be `v17.6` WIP, iteration 21). There will be a separate "Experimental Channel" in the cutting edge, but this is out of scope for this post.

### New Module Template: `17000`
Due to some oddities to FBE, the path Magisk used to store persist files (`/data/adb`) cannot be created/accessed in custom recoveries if the folder/data decryption does not exist. Magisk has to install files to an alternative path, and the new template is updated for this change, which at the same time prevents corrupting data on FBE when installing in custom recoveries.

### Install to Inactive Slot is Back!
Due to some changes in the Pixel OTA engines, the feature to install Magisk to inactive slots after OTA was broken for quite a while. This update added the ability for Magisk to force a slot swap using `bootctl`, so this super fascinating feature (that I personally do use a lot) is now back!

### SafetyNet Check is Back!
People are panicking about the "Invalid Response" of SN checks in Magisk Manager. It is actually just a cosmetic issue as Google banned the old API (which Magisk Manager and tons of SN apps in Play Store was still using).  
I'm well aware of several games in the wild was recently updated to detect Magisk yet again, I'll focus on that after this stable release, no worries!

### Highlights
For those that were on the stable channel, here is a highlight of what has changed from `v16.0` to `v17.0`

- Android Pie (9.0) support 
- Support targeting sub services when selecting an app to hide with MagiskHide, meaning background services of hidden apps would not be able to detect root
- Fix root loss issue when MagiskHide is enabled
- Support Samsung S9/S9+/Note 9
- And of course, tons of bug fixes and improvements you're not aware of :)

### Full Changelog: [here](https://forum.xda-developers.com/showpost.php?p=68966755&postcount=2)
