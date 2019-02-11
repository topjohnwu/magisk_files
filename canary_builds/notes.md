# Magisk (e05cdc83) (18104)
- Move sbin tmpfs overlay creation to early-init magiskinit daemon: simplify `magisk` startup
- Harden socket protection: no other binary other than the exact same `magisk` binary which started the server can access sockets. This is not only a security feature, but also mitigates some known detection methods
- Remove `magisklogd`: logcat gobbling is now completely handled within the same `magiskd` process
- Use timestamps to skip old logs instead of clearing the whole logcat buffer when failure
- Only try one time after unexpected logcat output EOF
- Overall, the code handling logcat is completely rewritten from scratch
- (18103) Fix boot loop on non system-as-root devices
- (18104) Fix EMUI 9 support

# Magisk Manager (b3140276) (186)
- Update to public release
- UI adjustments: make UI responsive so text will not overlap other components
- Add DirectBoot support to receivers and SuRequestActivity
