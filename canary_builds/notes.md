## Magisk (411ea56a) (17309)
- Mount `magisk.img` with `noatime` flag for better performance
- Add `FLAG_INCLUDE_STOPPED_PACKAGES` in broadcasts to force Magisk Manager to accept requests
- Fully migrate Magisk to C++

## Magisk Manager (9b063856) (155)
- Support managing `magisk.db` completely via cmdline
- Fix a bug when root is always denied for the first time when granting permission in the user dialog
- Revert dark theme adjustments
- Update PayPal donation link
- Upgrade snet extension pack
