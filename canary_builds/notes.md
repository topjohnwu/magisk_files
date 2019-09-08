## Magisk (087b451e) (19308)
- Fix a bug when `/product` does not exist, but `/system/product` does
- Fix `su_info` cache bug, causing consecutive `su` calls failing

## Magisk Manager (86481c74) (233)
- Remove option to cache module zips
- Allow users to select whether to use recovery mode or not.
This allows A-only system-as-root users manually patch recovery images without recovery_dtbo.
