## Magisk (c1602d25) (19301)
- Get UID from data folder instead of parsing `packages.xml`, should simplify the process and prevent crashes
- Properly implement namespace isolation in MagiskSU

## Magisk Manager (16b232d2) (216)
- Fix MagiskDB implementation: should fix logging, root settings, root policy changes, app package repackaging (Magisk Manager hide feature)
- Release builds are now back to fully obfuscated now :)
