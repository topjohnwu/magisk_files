## Magisk (80cd85b0) (19102)
- Add support for hi6250 devices
- Fix uninstaller scripts
- Fix modules not working on devices with `/data` also mounted with `tmpfs`
- Stop claiming device focus for su logging/notify if feasible.
This fix issues with users locking Magisk Manager with app lock, and prevent
video apps get messed up when an app is requesting root in the background.

## Magisk Manager (80cd85b0) (211)
- Fix locale settings not working properly
- Fix MagiskHide list not properly sorted
