# 2019.6.4 Magisk v19.3
The source code of Magisk Manager on `master` is still not ready for publish, so it will come later in the future.
This release should be the last stable v19 release. Starting from the next release, more advantageous changes will be added and beta tested.

## Magisk v19.3
- [MagiskHide] Hugely improve process monitor implementation, hopefully should no longer cause 100% CPU and daemon crashes
- [MagiskInit] Wait for partitions to be ready for early mount, should fix bootloops on a handful of devices
- [MagiskInit] Support EROFS used in EMUI 9.1
- [MagiskSU] Properly implement mount namespace isolation
- [MagiskBoot] Proper checksum calculation for header v2

### Full Changelog: [here](https://forum.xda-developers.com/showpost.php?p=68966755&postcount=2)
