## Magisk (523e6629) (18003)
- Support EMUI 9.0: patch `recovery_ramdisk.img` with Magisk Manager, and install with `fastboot flash recovery_ramdisk <patched image>`.
In order to boot with Magisk, you have to always reboot to recovery (press volume up while booting)
- Simplify `su_info` caching system
- Remove requirement of system C++ STL, use internal `new` and `delete` implementation

## Magisk Manager (523e6629) (170)
- Support EMUI 9.0
- The "Reboot" button will reboot to recovery if EMUI 9.0 is detected
