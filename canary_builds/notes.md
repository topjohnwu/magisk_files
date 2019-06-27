## Magisk (dd6e55ac) (19303)
- 100% complete MagiskInit rewrite for system-as-root devices.
The system partition is now the actual root directory (`/`) as it was designed!!
- Fully support latest Android Q Beta 4: new SAR implementation + rewritten process monitor for MagiskHide.
Logical partition (Pixel 3 on Q) is coming next!

## Magisk Manager (dd6e55ac) (226)
- Update scripts to prevent bootlooping the new SAR setup on boot
- Add reboot to EDL, and tweaked several reboot options
