## 2018.10.22 Magisk v17.3
(XDA Post: [here](https://forum.xda-developers.com/showpost.php?p=77933549&postcount=47))

(A hot fix with some minor changes is published with verison code `17302`, the version number is the same, v17.3)

Welcome to the Magisk family, Pixel 3!

I originally planned to do more changes to Magisk Manager before a new public release, but I think people can't wait to root their shiny new Pixel 3, so here we go!

### Up-to-date Documentations
Some subtle details, design choices, developer guides are all added to the documentations!

For most average users though, the most interesting part would be the tutorial: **Best Practices for MagiskHide**, please take some time and check it out!

[Magisk Documentations](https://topjohnwu.github.io/Magisk/)

### Boot Image Header v1
Google updated the boot image header format from `v0` to `v1` and was first used on the Pixel 3. The new header supports recovery DTBOs, which won't be used on any A/B devices, including Pixel 3 so that isn't the main issue here. The new format stores its version number to an originally unused entry in the header to determine whether the extended header entries is used. However in some freaking devices like Samsung's, they have been using the supposedly "unused" entry as the size of an non-AOSP "extra section" for quite a long time. `magiskboot` is designed to support extracting these extra sections (because people use Samsung), but with the introduction of header v1, the tool couldn't interpret the image properly, and thus generating invalid boot images.

`magiskboot`'s boot image parsing, unpacking and repacking code was rewritten with C++ to utilize the more powerful language features due to the complexity (because I still need to support freaking `PXA` format headers used by old Samsung devices...)

### MagiskSU Rewrite
Both the daemon and client side of MagiskSU is completely rewritten with improvements and optimizations, for example: simplified `su_info` caches, early ACK between daemon and client to prevent process freezing when denied, sending parsed command-line options instead of full arguments, and many more!

### Samsung Defex Patches
A hexpatch for removing Samsung's new KNOX feature: Defex Safeplace was actually already introduced in previous releases, but that solution wasn't ideal since each new kernel release would generate different patterns. A more general patch (which is only a single CPU instruction!) was discovered and included into this new release.

### Magisk-Modules-Repo Moderation
If you aren't aware, a team of zealous volunteer moderators were already starting to review new submission manually, being the gate keeper of our beloved Magisk-Modules-Repo. Hopefully this will prevent pointless/spam modules polluting the download section in Magisk Manager!

### Full Changelog: [here](https://forum.xda-developers.com/showpost.php?p=68966755&postcount=2)
