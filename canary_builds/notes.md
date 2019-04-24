## Magisk (54d1207f) (19005)
- For detecting volume up: track all input devices that is supported. In theory should support more devices such as unlocked Snapdragon S10s
- Monitor `app_process` binary usage in case multiple zygote daemons are spawned
- Simplify `/sbin` `tmpfs` overlay setup: all procedures are now done in pre-init stage, could fix some bootloop issues on some devices

## Magisk Manager (54d1207f) (207)
- Upgrade `libsu`
- Update `post_ota.sh`
