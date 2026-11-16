# Time Tracker releases

Public download and update channel for Time Tracker.

This repository holds **notarized app builds** and the Sparkle `appcast.xml` only. Source code lives in a private repo.

## Sparkle feed

`SUFeedURL` in the app points to:

https://github.com/Bygg-Digitalt-AS/TimeTracker-releases/releases/latest/download/appcast.xml

## Publishing a build

1. Archive and export a Developer ID–signed, notarized `.app`.
2. Zip it (for example `TimeTracker-0.1.0.zip`).
3. Sign the zip with Sparkle `sign_update` and put the signature in `appcast.xml`.
4. Create a GitHub Release and attach both the zip and `appcast.xml`.
