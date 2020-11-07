## Magisk (dc5e78e1) (21006)
- Fix `lz4_lg` boot image unpacking/repacking
- Support unpacking/repacking vendor boot images
- Support kernel initialized dm-verity on legacy SAR
- Significantly broaden sepolicy.rule compatibility, now tries the following partitions for storing the rule files:
`unencrypted data` -> `FBE data` -> `cache` -> `metadata` -> `persist`
- Properly handle factory reset cases on Android 11
- Add magisk binaries to `PATH` in boot scripts

## Magisk Manager (dc5e78e1) (312)
- Fix crashes when network error occurs
- Tapjacking protection
