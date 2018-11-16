## Magisk (ab5fedda) (17316)
- Deprecate `/sbin/.core`, switch to `/sbin/.magisk`
- Deprecate `<mount_point>/.core`, nothing should be stored there. Details in the follwing.
- post-fd-data.d scripts are moved to `/data/adb/post-fs-data.d`, and service.d scripts are moved to `/data/adb/service.d`
- Native systemless hosts are removed. There is a new built-in module in Magisk Manager to serve the exact same functionality.
- All deprecated paths above are still accessible; the old paths will be replaced with symlinks to the new paths
- New option to `magiskhide`: `--status`. Use it to check MagiskHide status
- MagiskHide configs are moved to `magisk.db`
- `magisk.db` is handled by `magiskd` with a single long-lived connection. No other process should access the database concurrently.

## Magisk Manager (ab5fedda) (157)
- Add built-in Systemless Hosts module to replace the old method. Enable it in Settings.
