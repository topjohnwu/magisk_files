## Magisk (ec472309) (17317)
- Update multiple external dependencies
- Fix a bug causing `SIGWINCH` (terminal window size change) not followed
- Remove `/.backup` folder on boot so it can not be used for detection
- Use component names as MagiskHide targets. This allows MagiskHide to target all possible processes from an application.
- Fix a bug that caused Magisk Manager hiding errors

## Magisk Manager (ec472309) (158)
- Update translations
- Read install config from `/sbin/.magisk/config` since `/.backup` no longer exists
