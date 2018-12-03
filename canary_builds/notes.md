## Magisk (07bfdf3e) (17319)
- MagiskPolicy massive upgrade: more features
- Remove all `AUDITDENY` when applying Magisk rules so all AVC rejections will be logged

## Magisk Manager (07bfdf3e) (160)
- No longer uses platform `DownloadManager`: all downloads are handled manually.
This should prevent delays (sometimes download won't even start!) caused by high system usage
- Rich notifications when downloading modules, Magisk zip, and Magisk Manager
- Rich notifications when hiding Magisk Manager / restoring Magisk Manager
- Say goodbye to the deprecated `ProgressDialog`!
