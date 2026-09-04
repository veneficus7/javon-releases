# Jawon — Privacy Policy

**Last updated: 4 September 2026**

Jawon is a music player for music you already own. It has no accounts, no server
of its own, and no analytics. This policy describes everything it does with your
data, which is not much — and the parts that are not "nothing" are set out plainly
rather than buried.

---

## The short version

Jawon **collects nothing about you.** There is no account to create, no profile,
no advertising, no tracking, no analytics, and no telemetry of any kind. Nobody —
including the developer — can see your library, your listening history, or that
you use the app at all.

Your music, your shelves, the covers you choose and your play history live **on
your phone** and nowhere else. Uninstalling Jawon deletes all of it.

Jawon makes network requests in exactly **three** situations, all described below.
Two of them can be switched off, both are about looking up information for a
record you already own, and none of them sends anything that identifies you.

---

## What stays on your phone

All of this is stored in Jawon's private storage, which no other app can read:

- **Your library** — the shelves you create, the albums you import, their titles,
  artists, track lists and technical details, and where each case sits on the wall.
- **Cover images** — copied into Jawon's storage so the wall still renders if the
  original file moves.
- **Your listening history** — which album was played, when, and for how long. This
  is what the listening record and the wear on each case are drawn from.
- **Your settings** — room mode, crossfade, equaliser and effects, and the two
  lookup switches below.
- **Lyrics** fetched from LRCLIB, cached so the same track is never looked up twice.
- **Crash reports**, if the app has crashed. These stay on your phone unless you
  choose to send one — see below.

**None of this is transmitted anywhere.** Jawon operates no server, so there is
nowhere for it to go.

If you make a backup (Settings → Your library), Jawon writes a `.zip` to a
location **you** pick with the system file picker. That file is yours; Jawon does
not upload it and cannot see where you put it.

---

## The three times Jawon uses the network

### 1. Cover art lookup — on by default, can be switched off

**When:** during import, and only for albums whose own files carry no artwork.

**What is sent:** the album's **title** and **artist**, to
[MusicBrainz](https://musicbrainz.org). If a confident match comes back, Jawon
downloads that album's cover image from the
[Cover Art Archive](https://coverartarchive.org).

**What is not sent:** no account, no device identifier, no list of what else is in
your library, and nothing at all for albums that already have artwork.

**Switch it off:** Settings → Your library → *Look up cover art*. With it off,
Jawon never contacts either service, and albums without artwork simply show none
until you set one yourself.

### 2. Lyrics lookup — on by default, can be switched off

**When:** only when you open the lyrics page for a track whose own file contains no
lyrics and which has no `.lrc` file beside it.

**What is sent:** the track's **title**, **artist**, **album** and **length**, to
[LRCLIB](https://lrclib.net). The length is what distinguishes an album cut from a
single edit.

**What is not sent:** no account, no device identifier, no listing of your library.
The answer is stored on your phone so the same track is never asked about twice —
including when the answer is "no lyrics found".

**Switch it off:** Settings → Your library → *Look up lyrics*.

### 3. Checking for a new version — only when you ask

**When:** only when you press *Check for updates* in Settings. Jawon never checks
on its own, in the background, or on launch.

**What is sent:** nothing about you. Jawon requests a small public file from
GitHub listing the newest version, and if you choose to update, downloads that
release. Your installed version is compared **on your phone**, not by a server.

This applies to builds installed directly. If you installed Jawon from an app
store, that store handles updates instead.

### One thing that is true of all three

Any request over the internet necessarily reveals your device's **IP address** to
the server receiving it, along with a line identifying the app and its version.
This is how the internet works and is not something an app can avoid — but it
would be misleading to say "nothing leaves your device" without naming it.

MusicBrainz, the Cover Art Archive, LRCLIB and GitHub are independent
organisations with their own privacy policies. Jawon sends them only what is
described above.

---

## Crash reports

If Jawon crashes, it writes what went wrong to a file on your phone: the error,
the version of the app, and your phone's model and Android version. **It is not
sent anywhere.**

Settings → *Problems* shows you that file in full, and offers a **Send** button
that hands it to an app you choose — email, a messenger, wherever you like. That
only ever happens because you pressed it, and you can read the entire contents
first. **Clear** deletes it.

Crash reports contain no personal information and no details of your library. They
contain a technical description of a fault, and they exist because there is
otherwise no way for the developer to learn that Jawon broke on your phone.

---

## Permissions, and why

| Permission | Why |
|---|---|
| **Music and audio** (`READ_MEDIA_AUDIO`, or `READ_EXTERNAL_STORAGE` on Android 9–12) | To find music already on your phone. Read-only, and **audio only** — Jawon never requests photos, video, or general file access. You can decline it and still add music with the folder picker. |
| **Internet** | The three lookups above, and nothing else. |
| **Notifications** | To show the playback notification with the track and its controls. |
| **Foreground service** | To keep playing when the screen is off, which is what a music player is for. |
| **Vibrate** | The tick you feel when turning the disc to scrub. |
| **Modify audio settings** | To attach the equaliser and effects to Jawon's own playback. It cannot change any other app's audio. |
| **Install unknown apps** | Only for the self-update above, and only on directly-installed builds. Android always shows its own confirmation; Jawon cannot install anything silently. |

Jawon requests no location, no contacts, no camera, no microphone, and no phone
identifiers.

---

## Children

Jawon is not directed at children and collects no information from anyone,
including children.

---

## Deleting your data

Everything is on your phone, so you control all of it:

- Remove an album from the room, and its record and cover are deleted.
- Clear a crash report in Settings → Problems.
- **Uninstall Jawon**, and every trace of it is removed — library, covers, history
  and settings. There is no copy anywhere else, because there is no anywhere else.

There is no account to close, and no request to make of anyone.

---

## Changes to this policy

If Jawon ever does something new with data, this policy will be updated before
that version ships, and the date at the top will change. Anything that would send
something not listed here would be a new feature with its own switch, described
in the app before it did anything.

## Contact

Questions about this policy, or about anything above:
**bakhodirmurodillaev@gmail.com**
