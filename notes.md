## Magisk (b1dbbdef) (21404)

- [MagiskInit] Fix bootloops on legacy rootfs devices
- [General] Remove unneeded busybox redirection

### How to Use the APK for Recoveries

In general, it is recommended to install and uninstall Magisk through the Magisk app.
However, if you insist to use custom recoveries, rename the Magisk APK's `.apk` file extension to `.zip`.
TWRP should then be able to directly flash the zip file.
If you have trouble renaming the file extension on PC, rename the file with TWRP's built-in file manager.
To uninstall in recovery, rename the zip file to `uninstall.zip` before flashing it.

## Diff from v21.4

- [General] Magisk and Magisk Manager is now merged
- [General] The app name is changed from "Magisk Manager" to simply "Magisk".
If you are currently hiding Magisk Manager, you would need to un-hide and re-hide to have the app label renamed properly.
- [MagiskHide] Fix a bug when stopping MagiskHide does not take effect
