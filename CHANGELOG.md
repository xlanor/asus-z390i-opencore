# 0.6.3-0.6.6
- Bumped Opencore from 0.63-0.6.6
- Added new keys in 0.6.6
- Switch Driver from `HFSPlus` to `OpenHFSPlus`
- Removed `DeduplicateBootOrder`
- Switched from `Bootstrap` to `LauncherOption`. Read `0.63-0.66.md` for more information.

# 0.6.6-0.6.9
- Bumped Opencore from 0.6.6-0.6.9
- Added new keys from 0.6.9 sample config
- Re-enabled SIP in order for System Update to work.
- Added OpenCanopy (which became native in 0.6.7) for a nicer OpenCore experience.
- Disabled XhciPortLimit because we already have mapped USBs. And 11.3 behaves really weirdly with it.
- Bumped MacOS to 11.4-alpha3 (20F5065a), Developer Preview Build.

# 0.69-11.4
- Updated to release version of 11.4 with no obvious issues so far.
