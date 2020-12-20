## Magisk (d0896984) (21102)
- Make sure post-fs-data scripts never block over 35 seconds
- Make sure boot stages never run in parallel
- Improve device compatibility by detecting 2SI later on legacy SAR devices
- Handle Windows file endline more gracefully
- No longer uses `logcat` to dump logs to files. Directly log to files internally.


## Magisk Manager (d0896984) (316)
- A large number of small patches here and there
