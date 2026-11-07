# Universus Simulator: client builds

Hand-delivered builds of the Universus Simulator client, one zip per platform. Download the one for your machine, unzip it anywhere, and read the section below for it: every platform blocks an unsigned download the first time in its own way, and none of them explain themselves.

You will need a [tcgs.io account](https://tcgs.io?game=universus) and a deck of your own. Card art is fetched as you go, so the first run wants an internet connection.

## Downloads

| Platform | File | Size | Built (UTC) |
| --- | --- | --- | --- |
| linux | [linux.zip](https://github.com/tkfnetwork/universus-simulator-clients/raw/main/linux.zip) | 69 MB | 2026-11-07T21:20Z |
| macos-arm64 | [macos-arm64.zip](https://github.com/tkfnetwork/universus-simulator-clients/raw/main/macos-arm64.zip) | 69 MB | 2026-11-07T21:21Z |
| macos-x86_64 | [macos-x86_64.zip](https://github.com/tkfnetwork/universus-simulator-clients/raw/main/macos-x86_64.zip) | 73 MB | 2026-11-07T21:21Z |
| windows | [windows.zip](https://github.com/tkfnetwork/universus-simulator-clients/raw/main/windows.zip) | 79 MB | 2026-11-07T21:20Z |

macOS comes as two downloads, one per processor: **macos-arm64** for Apple Silicon, which is every Mac from late 2020 onwards, and **macos-x86_64** for an Intel Mac. If you are not sure, the Apple menu, then About This Mac, names the chip.

Check a download against what was built:

```
29842e931166fcf10fb129369875ca35683c149418e7fb1229b9b361a667a3e8  linux.zip
a2c820107ad2306205f9c29c36e748ed5a714bff77383319a46b9051aac68932  macos-arm64.zip
ebb55a955595b7a44173cf280d1805651a0d9ada5320c17f0dab419f388fcba6  macos-x86_64.zip
fcbba5a43c07e2bf8e4cd1bb584a94865f8b66e85548e1106541f2ca7bcf2e81  windows.zip
```

## What is in these builds

| Platform | Version | Engine | Access | Channel | Relay | API | Built-in deck |
| --- | --- | --- | --- | --- | --- | --- | --- |
| linux | 0.0.5 | 4.7.2.stable.mono.arch_linux.ed1daf0bf | restricted | ALPHA | hosted | default | false |
| macos-arm64 | 0.0.5 | 4.7.2.stable.mono.arch_linux.ed1daf0bf | restricted | ALPHA | hosted | default | false |
| macos-x86_64 | 0.0.5 | 4.7.2.stable.mono.arch_linux.ed1daf0bf | restricted | ALPHA | hosted | default | false |
| windows | 0.0.5 | 4.7.2.stable.mono.arch_linux.ed1daf0bf | restricted | ALPHA | hosted | default | false |

What changed in each version is in [CHANGELOG.md](CHANGELOG.md). The version a build is stamped with is also written across the bottom of its home screen, in the middle, next to the commit it came from.

An `open` build lets anyone play, signed in or not. A `restricted` build is gated by login: it wants a tcgs.io account that has been granted access to this client, and signs everyone else out. A relay of `local only` means the client looks for one on the player's own machine, so that build can only pair with somebody sitting at it; `hosted` means it reaches one over the network and needs no setup.

## First run on linux

```
Universus Simulator for Linux
=============================

Unzip anywhere and run:

    ./UniversusSimulator.x86_64

If it refuses with "permission denied", the zip lost the executable bit on the
way to you. Restore it once:

    chmod +x UniversusSimulator.x86_64

Nothing needs installing: the game, its cards and the .NET runtime are all in
the one file.


What you need to play
---------------------

An account at https://tcgs.io?game=universus, and a deck of your own. Card art
is fetched as you go, so the first run wants an internet connection.
```

## First run on macos

```
Universus Simulator for macOS
=============================

There are two downloads, one per processor. macos-arm64 is for Apple Silicon,
which is every Mac from late 2020 onwards; macos-x86_64 is for an Intel Mac.
The Apple menu, then About This Mac, names the chip. The wrong one will not
start, and it fails in a way that looks like the block below rather than like
the mismatch it is.


macOS will refuse to open this the first time. That is expected, and it is not
a sign that anything is wrong with the download. It happens because the app is
signed but not notarized, and notarizing needs an Apple Developer account.

You only have to do this once.


The quick way (any macOS version)
---------------------------------

Open Terminal, type the following, then drag the app onto the Terminal window
so it fills in the path for you, and press Return:

    xattr -dr com.apple.quarantine 

It prints nothing when it works. Now open the app normally.


The clicking way (macOS 15 Sequoia and later)
---------------------------------------------

1. Double-click the app. macOS says it "cannot verify" the app. Click Done.
2. Open System Settings, then Privacy & Security.
3. Scroll to the bottom. There is a line saying the app was blocked, with an
   "Open Anyway" button. Click it.
4. Confirm with Touch ID or your password, then click "Open Anyway" again.

Older macOS (14 Sonoma and earlier) instead lets you right-click the app,
choose Open, and then Open again in the dialog. Apple removed that shortcut in
Sequoia, which is why the steps above go through System Settings.


If it just opens
----------------

Then macOS never flagged it, which happens when the file reached you without
going through a browser or a mail client. Nothing else to do.


What you need to play
---------------------

An account at https://tcgs.io?game=universus, and a deck of your own. Card art
is fetched as you go, so the first run wants an internet connection.
```

## First run on windows

```
Universus Simulator for Windows
===============================

Unzip anywhere and run UniversusSimulator.exe.

The first time, Windows will say "Windows protected your PC" and offer only a
"Don't run" button. That is expected, and it is not a sign that anything is
wrong with the download. It happens because the .exe is not signed, and signing
needs a certificate bought from a certificate authority.

Click "More info", then "Run anyway". You only have to do this once.

Nothing needs installing: the game, its cards and the .NET runtime are all in
the one file.


What you need to play
---------------------

An account at https://tcgs.io?game=universus, and a deck of your own. Card art
is fetched as you go, so the first run wants an internet connection.
```

## Copyright

These builds ship no UniVersus artwork: card images are fetched from tcgs.io as they are shown.

UniVersus, and any and all material belonging to it, is copyright UVS Games. No ownership of it is claimed here. This is an unofficial client, and is not affiliated with, endorsed by or sponsored by UVS Games.
