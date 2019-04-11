## Magisk (8d4c4072) (19004)
- Don't allow adding new files in mount point roots (`/system` and `/vendor`)
- Use our own devices nodes for mounting mirrors and modules to keep track of custom mounts
- Directly start activities in Magisk Manager for native-app communication. This better supports Android Q and also workaround many Chinese ROM broadcast restrictions added to the system

## Magisk Manager (8d4c4072) (206)
- Fix patch boot image on non-rooted devices
- Remove patch format options as it now uses the same format as the input file
- Allow multiple modules to be downloaded at the same time
- Lock orientation of `SuRequestActivity` so the dialog will not be destroyed when changing orientation
- Support new native-app communication from native Magisk
