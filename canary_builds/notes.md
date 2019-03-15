## Magisk (8893cbd6) (18119)
- Support boot image header v2
- Make sure files in `rootfs` is properly labeled with correct context:
Android Q init assumes root directory to always reside in system
partitions and never run restorecon to restore `rootfs` selabels.
We have to do it ourselves
- Support Android Q split policy setup
- Add new `--load-split` option to `magiskpolicy`

## Magisk Manager (8893cbd6) (199)
- Fix a bug that settings don't reflect real configs
- Prevent SafetyNet from being removed from hide list
