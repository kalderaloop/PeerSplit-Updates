# PeerSplit Updates

This public repository contains signed PeerSplit Android update assets and the measured `update.json` manifest only.

## Layout

- `update.json`: current anonymous update manifest used by the app;
- `releases/<tag>/peersplit-<version>.apk`: immutable, stable-signed APK for a published version.

The private source repository publishes these files through a deploy key that can write only to this repository. Existing release directories are never overwritten.

The application source, signing material, passwords, private keys, OAuth data and cloud capability data are not stored here.

PeerSplit verifies the APK checksum, Android package name, version code and signing certificate before opening Android's system installer. Android still requires the user to confirm installation.
