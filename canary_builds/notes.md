## Magisk (b7f69238) (18007)
- Change the way update-binary is bundled
- Switch to use STL (llvm libc++)
- Support down to Android 4.2 (with resetprop, magiskhide, and modules force disabled)
- Fix segfault on several devices

## Magisk Manager (118a9f22) (178)
- Minimize memory usage for verify and sign boot images
- Do not show incorrect progress when content length is not available when downloading files
- Preserve the su timeout after user selection, so it will not always start at "Forever"
- Many other under-the-hood optimizations
- Fix crash when starting Magisk Manager with clean data
