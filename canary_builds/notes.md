## Magisk (d64d12af) (19306)
- Use relative symlinks internally (fix several minor issues)
- Use C++ `shared_ptr` instead of manual reference counting in `su_info` caching
- Unblock all signals when creating root shell
- Better randomization: all random strings in Magisk will now also have random length
- Several sepolicy rule updates for Q and new SAR implementation
- Introduce new root overlay system that is compatible with new SAR

## Magisk Manager (f1112fdf) (228)
- Update scripts to recognize logical partition system-as-root
