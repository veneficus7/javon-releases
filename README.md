# Jawon — beta builds

Release APKs for [Jawon](https://github.com/veneficus7/jawon), a local-first
Android music player where the library is a room rather than a list.

**The source is at [veneficus7/jawon](https://github.com/veneficus7/jawon).** This
repository holds only the signed APKs and `latest.json`, the manifest the app reads
when it checks for its own updates.

## Installing

Download the APK from [Releases](https://github.com/veneficus7/javon-releases/releases)
and open it. Android will ask you to allow installing apps from this source; that
is the normal prompt for anything not from the Play Store.

Requires **Android 9 or newer**.

After the first install, Jawon can update itself: **Settings → Check for
updates**. Nothing happens on its own — checking, downloading and installing are
each a deliberate tap.

## What `latest.json` is

The manifest the app reads. `versionCode` is what decides whether a build counts
as an update; the app compares that number and nothing else.

## Verifying a build

Every release is signed with the same key. You can check one before installing:

```bash
apksigner verify --print-certs jawon-0.4-beta.apk
```

```
CN=Bakhodirjon Murodillaev, OU=Jawon, O=Veneficus, L=Suwon, ST=Gyeonggi-do, C=KR
SHA-256: 8c74a0400a79122041876e47c0bf98912ff257a084c656b20a6bb23a8f9f8766
```

Android enforces this itself: an APK signed with any other key cannot replace an
installed Jawon. It can only fail to install.
