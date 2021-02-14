## Magisk (b76c80e2) (21410)

- [App] Fix crashes after hiding the Magisk app
- [MagiskSU] Fix incorrect APEX paths that caused `libsqlite.so` fail to load

### How to Use the APK for Recoveries

In general, it is recommended to install and uninstall Magisk through the Magisk app.
However, if you insist to use custom recoveries, rename the Magisk APK's `.apk` file extension to `.zip`.
TWRP should then be able to directly flash the zip file.
If you have trouble renaming the file extension on PC, rename the file with TWRP's built-in file manager.
To uninstall in recovery, rename the zip file to `uninstall.zip` before flashing it.

## Diff from v21.4

- [General] Magisk and Magisk Manager is now merged!
- [App] Rename the app "Magisk Manager" to "Magisk"
- [App] Support hiding the Magisk app with advanced technique (stub APK loading) on Android 5.0+ (it used to be 9.0+)
- [App] Disallow re-packaging the Magisk app on devices lower than Android 5.0
- [MagiskHide] Fix a bug when stopping MagiskHide does not take effect
- [MagiskBoot] Fix bug when unpacking `lz4_lg` compressed boot images
- [MagiskInit] Support Galaxy S21 series
- [MagiskSU] Fix incorrect APEX paths that caused `libsqlite.so` fail to load
