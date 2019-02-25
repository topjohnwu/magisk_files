## Magisk (8032bd0b) (18109)
- Modernize `magiskboot` code base for future maintenance
- Add compressed CPIO support: if the boot partition is too small
to fit in magisk patched boot image, we compress almost all of the
ramdisk with LZMA2(`xz` format) to give us more head room.
- Switch `magiskboot` to static binary and adjust the installation
script to support obscure and outdated custom recoveries. No more
messing with dynamic linkers when installing in recoveries.
- Add 64 bit binaries for `magisk`: all static binaries are still 32
bit to minimize binary sizes, but the main daemon that users 99%
of the time interacts and runs, `magisk`, is now running in native
64 bit!
- Auto clone attributes (owner, permissions, secontext) from existing
files to module files. This fool proof in case people do stupid things
or cannot properly create modules
- Introduce `/data` mirror: Since we switched to imageless Magisk,
module files are directly stored in /data. However, /data is mounted
with nosuid, which does not play well with files that requires special
secontext. Modules like Xposed should work properly now.

## Magisk Manager (8032bd0b) (189)
- Support 64 bit installs
