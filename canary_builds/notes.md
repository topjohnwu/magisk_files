# Magisk (6412bfc7) (18106)
- Completely new MagiskHide implementation! Massive kudos to [@arter97](https://twitter.com/arter97) for the initial contribution. This new process monitoring method is 100x more reliable, less crashes, and most importantly does not depend on logcat parsing! The basic idea is monitoring target APKs and filter processes with its UID.

# Magisk Manager (e5940168) (187)
- Move `minSdkVersion` to 17
- Update translations
