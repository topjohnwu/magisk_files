## Magisk (9b063856) (17306)
- Modify/create `magisk.db` completely natively within `magisk`
- Expose CLI in `magisk` to interact with `magisk.db` directly via SQL for Magisk Manager
- Make sure `magisklogd` is properly initialized before going further

## Magisk Manager (9b063856) (155)
- Support managing `magisk.db` completely via cmdline
- Fix a bug when root is always denied for the first time when granting permission in the user dialog
- Revert dark theme adjustments
- Update PayPal donation link
- Upgrade snet extension pack
