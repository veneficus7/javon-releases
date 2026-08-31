# Jawon — beta builds

Release APKs for [Jawon](https://github.com/veneficus7/javon), a local-first
Android music player where the library is a room rather than a list.

**The source lives in a private repository.** This one exists only so the app can
check for its own updates: an updater cannot authenticate to a private repo
without shipping a token inside the APK, where anyone could read it back out.

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
