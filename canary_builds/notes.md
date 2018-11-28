## Magisk (a9f265a5) (17318)
- Properly kill processes when initializing/add/remove targets from hide list
- Use raw `execve` for running external programs since some `libc` wrappers are problematic
- Add built-in procfs `hidepid=2` patch for devices vulnerable of the bug

## Magisk Manager (a9f265a5) (159)
- Rename application label to **Magic** to prevent detection
- Fix a bug that cause incorrect module UI if module does not have proper metadata
- Launch repackaged/restored Magisk Manager automatically (better user experience)
