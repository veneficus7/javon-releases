# Jawon — Privacy Policy

**Last updated: 21 September 2026**

Jawon is a music player for music you already own. It has no accounts, no server
of its own, and no analytics. This policy describes everything it does with your
data, which is not much — and the parts that are not "nothing" are set out plainly
rather than buried.

**What changed on 21 September 2026:** Jawon no longer connects to **Spotify**, so it
now uses the network in six situations rather than seven. If you connected Spotify in
an earlier version, the first time this version opens it erases the Client ID and the
sign-in tokens from your phone, and takes the Spotify albums off your wall along with
their covers and listening history. Nothing on the phone can withdraw Jawon's access
on Spotify's side: to do that as well, remove the app from the apps list in your
Spotify account settings.

**What changed on 11 September 2026:** new uses of the network, each described in
full below. Jawon has a **record shop** that browses and plays openly licensed music
from the Internet Archive (section 5), and it can **rip an audio CD** from a USB drive,
asking MusicBrainz what the disc is (section 6). Neither happens until you use it,
and Jawon still operates no server of its own. (A third, connecting Spotify, was added
the same day and removed on 21 September.)

**What changed on 8 September 2026:** Jawon can now play from a music server that
**you** run, so a library too large for your phone does not have to be on it. That
is a fourth use of the network, and it is described in full in section 4. It is off
until you set it up, and the server it talks to is one you choose and control —
Jawon still operates no server of its own.

---

## The short version

Jawon **collects nothing about you.** There is no account to create, no profile,
no advertising, no tracking, no analytics, and no telemetry of any kind. Nobody —
including the developer — can see your library, your listening history, or that
you use the app at all.

Your music, your shelves, the covers you choose and your play history live **on
your phone** and nowhere else. Uninstalling Jawon deletes all of it.

Jawon makes network requests in exactly **six** situations, all described below.
Two of them happen during ordinary use and each has its own switch: looking up cover
art, and looking up lyrics. The other four never happen until you act — pressing
*Check for updates*, setting up a music server, opening the record shop, or ripping a
CD. **None of them sends anything to the developer**, who runs no server and receives
nothing.

One of them is different in kind from the rest, because it involves an account of
yours, so it is worth saying plainly here rather than only in its own section: **a
music server of your own** sends **your username and password** to **an address you
typed in**, and streams your music back from it. That is a service **you** run and
control. Jawon does not choose it and does not know what is on it.

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
- **Your music server's address, username and password**, if you set one up. Stored
  in the same private storage as everything else here. The Subsonic protocol needs
  the password on every request, so it cannot be kept as a one-way hash the way a
  login secret could be — it is stored as you typed it. On a normal phone no other
  app can read it; on a rooted phone it is readable, and so is everything else in
  this list. Only ever sent to the server you nominated.
- **The catalogue from that server** — album and track titles, artists, lengths and
  one cover image each. This is what makes the wall render instantly and offline.
- **Albums from the record shop** that are on your wall — titles, artists, track
  lists, lengths and one cover image each, the same as any other album.
- **Recently streamed audio** from your server or the record shop, held in a
  size-limited cache so that turning the disc to scrub does not wait for the network.
  You set the size and can clear it at any time in Settings; the system may also
  delete it when your phone is short of space.

A **ripped CD** is not kept in Jawon's private storage at all: it is written as
ordinary audio files to a folder **you** pick, and then imported like any folder.

**None of this is transmitted to the developer, and none of it goes anywhere Jawon
chooses.** Jawon operates no server, so there is nowhere for it to go. The exception
is a music server you connect yourself, which receives exactly what section 4
describes.

If you make a backup (Settings → Your library), Jawon writes a `.zip` to a
location **you** pick with the system file picker. That file is yours; Jawon does
not upload it and cannot see where you put it.

---

## The six times Jawon uses the network

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

### 4. A music server of your own — off until you set it up

**When:** only if Jawon has a server to talk to. There are three ways it can get one,
and you can see and change all of them in Settings → *A music server of your own*:

1. **You type one in.** Nothing happens until you do.
2. **You paste a link** someone sent you, which fills in the same three fields at once.
3. **The copy of Jawon you installed came with one already set up.** Some builds are
   made for a specific shared library and ship pointed at it, so the app has music the
   first time it opens. When that is the case, the settings screen **says so**, and the
   address and username are shown to you there like any other. **FORGET** removes it
   permanently — it does not come back on the next launch.

With no server by any of those routes, none of this happens and Jawon behaves exactly as
it did before this feature existed.

**What this is for:** a library of hundreds of albums does not fit on most phones.
Pointing Jawon at a Subsonic-compatible server you run — Navidrome, Airsonic, Gonic,
Ampache — puts those albums on the wall without putting the audio on your phone.

**What is sent, and to whom:** your **username**, a **random salt**, and a
**one-way hash of your password combined with that salt**, to **the address you
entered and nowhere else**. This is how the Subsonic protocol authenticates; your
password itself does not cross the wire, and a captured request cannot be replayed.
Alongside it go requests for your album list, for cover images, and for the audio
of whatever you press play on.

**Who receives it:** whoever runs that server. If that is you, that is you. Jawon
does not know the address, does not report it anywhere, and has no relationship
with it. **This is the one place where what happens to your data depends on
somebody other than you** — so if the server is not yours, its operator can see
what you play and when, in the same way any server can. That applies most of all
to a build that arrived already pointed at somebody else's library: it is their
machine, their logs, and their rules, and Settings shows you the address so you can
decide whether you want to be on it.

**What is not sent:** nothing about your local library, nothing about albums stored
on the phone, no device identifier, and no account with the developer, because
there isn't one.

**Switch it off:** Settings → *A music server of your own* → **FORGET**. That
removes the address and credentials from your phone immediately. The albums stay on
the wall until you remove them, and simply stop playing — deleting hundreds of
records because a password was cleared would be a drastic reading of a small
action.

### 5. The record shop — only while you use it

**When:** only while you are browsing the record shop, and when you play a record you
found there or took home from it.

**What is sent:** to the [Internet Archive](https://archive.org), a non-profit
library: the words you type into the shop's search, the collection you are browsing,
and requests for the details and cover of the records you look at. When you play one,
its audio is streamed from the Archive; if you choose to keep an album on the phone
for offline listening, all of its tracks are fetched at once.

**What is not sent:** no account, because the Archive needs none; no device
identifier; and nothing about the rest of your library.

**Switch it off:** there is nothing running to switch off — the shop only talks to
the Archive while you are in it or playing something from it. Records you took home
stay on your wall like any other album until you remove them.

### 6. Identifying a CD you rip — only when you rip one

**When:** only on the CD screen, after you have connected a USB CD drive to your
phone, allowed Jawon to use it, and put an audio CD in.

**What is sent:** the disc's **disc ID** — a code worked out from the CD's track
layout, meaning how many tracks it has and where each one starts — to
[MusicBrainz](https://musicbrainz.org), which answers with the album's title, artist
and track names so the files can be named. Nothing else about the disc, and none of
its audio.

**Where the audio goes:** into a folder **you** pick, as ordinary audio files, which
Jawon then imports like any other folder. It is not uploaded anywhere.

**USB access:** Jawon cannot talk to a drive until Android's own dialog has asked you
and you have allowed it.

**A note on streaming services:** Spotify, SoundCloud, Apple Music and similar are
not supported, and this is not an omission to be fixed later: their developer terms
forbid an app from modifying the audio — and equalising it, filtering it and
scratching it with the disc is most of what Jawon does. An earlier version could
remote-control Spotify, which plays the sound in its own app; it was removed because
none of that could reach the music.

### One thing that is true of all six

Any request over the internet necessarily reveals your device's **IP address** to
the server receiving it, along with a line identifying the app and its version.
This is how the internet works and is not something an app can avoid — but it
would be misleading to say "nothing leaves your device" without naming it.

MusicBrainz, the Cover Art Archive, LRCLIB, GitHub and the Internet Archive are
independent organisations with their own privacy policies. Jawon sends
them only what is described above. A music server you set up is not an independent
organisation at all — it is a machine you chose, and its privacy policy is whatever
you decide it is.

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
| **Internet** | The six uses above, and nothing else: cover art, lyrics, the update check, a music server you set up yourself, the record shop, and identifying a CD you rip. |
| **USB devices** (not requested in advance) | To read an audio CD from a USB drive. Nothing is declared for this ahead of time: Android asks you in its own dialog, for that drive, when you connect one. |
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
- Clear the streamed-audio cache in Settings → *Offline store*.
- **FORGET** your music server in Settings, which erases its address and your
  credentials from the phone.
- **Uninstall Jawon**, and every trace of it is removed — library, covers, history,
  settings, cached audio and server credentials. There is no copy anywhere else,
  because there is no anywhere else.

There is no account with Jawon to close, and no request to make of anyone.

What uninstalling does **not** reach is anything outside the phone: a music server
you set up, which is yours and keeps whatever it keeps; the files of a CD you ripped,
which live in the folder you chose for them; and, if you connected Spotify in an
earlier version, your Spotify account, where you can remove Jawon's access from the
apps list in your account settings.

---

## Changes to this policy

If Jawon ever does something new with data, this policy will be updated before
that version ships, and the date at the top will change. Anything that would send
something not listed here would be a new feature with its own switch, described
in the app before it did anything.

## Contact

Questions about this policy, or about anything above:
**bakhodirmurodillaev@gmail.com**
