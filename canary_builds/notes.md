## Magisk (660e0dc0) (18108)
- Switch to monitoring `/data/system/packages.xml` instead of traversing `/data/app`. This should also fix issues with hiding system apps
- Fix bootloops when removing system root in Android < 5.0
- Add some SELinux rules for Samsung deodex ROMs
- Fix bootloops on devices with `init.rc` that has no newline at end of file (seriously, WTF are these OEMs doing)
- (18108) Fix MagiskHide unmount failures

## Magisk Manager (3ebc886f) (188)
- Update translations
