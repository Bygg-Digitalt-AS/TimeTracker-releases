# Time Tracker releases

Public download and update channel for Time Tracker.

This repository holds **notarized app builds** and the Sparkle `appcast.xml` only. Source code lives in a private repo.

## Sparkle feed

https://github.com/Bygg-Digitalt-AS/TimeTracker-releases/releases/latest/download/appcast.xml

## Publish a build

From the private Time Tracker repo on a Mac that has:

1. **Developer ID Application** certificate (Xcode → Settings → Accounts → Manage Certificates)
2. Notary credentials stored as `TimeTracker-notary`
3. Sparkle EdDSA private key in the login keychain

Run:

```bash
./scripts/publish-direct.sh
```

That archives a Release build (sandbox off), notarizes it, generates a Sparkle-signed zip + `appcast.xml`, and creates a GitHub Release here with both files attached.

Bump `CURRENT_PROJECT_VERSION` before each publish so Sparkle sees a newer build.
