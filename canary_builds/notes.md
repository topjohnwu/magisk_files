## Magisk (c1602d25) (19301)
- Get UID from data folder instead of parsing `packages.xml`, should simplify the process and prevent crashes
- Properly implement namespace isolation in MagiskSU

## Magisk Manager (12bbc7fd) (223)
- Fix blank Superuser fragment under some circumstances
- Fix incomplete repo database bug: if you experience this issue from the old version, go to Settings → Clear Repo Cache and refresh the Download fragment
- Fix crashing when pressing fast scrolling button when logs are empty
