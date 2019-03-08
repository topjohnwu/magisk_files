## Magisk (0204d053) (18114)
- Zygote ptrace-ing MagiskHide: APK inotify based process monitoring
is shown to be sometimes too slow for hijacking apps. As a result, I
rewritten MagiskHide 100% from scratch, again, with a new implementation.
This new implementation will use the `ptrace` Linux API to monitor zygote,
which effectively hijacks a target app **before** it is even started.
- MagiskHide now accepts different apps with the same process as separate
targets. This allows MicroG DroidGuard helper to be also added to the
default hide list.
- Support Android Q's new init setup
- Several `magiskboot` improvements (for dev use only)
- (18114) Remove zygote notifier (will find better ways to detect zygote in the future)

## Magisk Manager (c345633d) (194)
- Fix Magisk Hide fragment crashing on Android lower than Nougat
