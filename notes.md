## Magisk (bf80b08b) (22003)

- Rebuild executables (fix boot image repacking issues)

## Diffs to v22.0

- [App] Prevent multiple installation sessions running in parallel
- [App] Prevent OutOfMemory crashes when checking boot signature on PXA boot images
- [General] Proper cgroup migration implementation
- [General] Prevent possible deadlock in logging code
- [MagiskBoot] Preserve and patch AVB 2.0 structures/headers in boot images
