## 2018.9.21 Magisk v17.2
(XDA Post: [here](https://forum.xda-developers.com/showpost.php?p=77678063&postcount=46))

Unexpected early release due to a bug in Magisk Manager that never surfaced until some online repo triggered it LOL. But well this means you get several sweet features early too :)

### Magisk Manager Obfuscation
There are some detection method out in the wild that analyzes all installed APK to find signs of Magisk Manager to mitigate the package name randomization feature within the app. The counter-counter-attack here is to do excessive obfuscation so it can no longer do so.

### New Communication Scheme
However, for full obfuscation to be possible, it creates some issues. In MagiskSU's code, some Java class names in Magisk Manager are hardcoded as destinations to send requests and logging information. A completely new communication scheme is written from scratch to eliminate any class name assumptions in MagiskSU, so that 100% Magisk Manager obfuscation is achievable. This current release (Magisk Manager 6.0.0), however, is not built with full obfuscation due to the requirement to be backwards compatible with v17.1.

### Randomize Service Names
Magisk injects several init services to startup the daemon. Some apps are updated to detect these specific service names to determine whether Magisk services are running on your device. MagiskInit is updated to randomly generate service names pre-init, so every time your device reboots it will use a different service name.

### Updated Resetprop
Android Pie introduced a new type of system property format that previous resetprop is not able to handle. Several properties, for example device fingerprint props, are therefore unable to be modified (many people modify device fingerprint to pass CTS). Resetprop is updated to use the upstream AOSP code base to process system properties.

### Full Changelog: [here](https://forum.xda-developers.com/showpost.php?p=68966755&postcount=2)
