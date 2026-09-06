# Universus Simulator: client builds

Hand-delivered builds of the Universus Simulator client, one zip per platform. Download the one for your machine, unzip it anywhere, and read the section below for it: every platform blocks an unsigned download the first time in its own way, and none of them explain themselves.

You will need a [tcgs.io account](https://tcgs.io?game=universus) and a deck of your own. Card art is fetched as you go, so the first run wants an internet connection.

## Downloads

| Platform | File | Size | Built (UTC) |
| --- | --- | --- | --- |
| linux | [linux.zip](linux.zip) | 69 MB | 2026-09-06T22:05Z |
| macos-arm64 | [macos-arm64.zip](macos-arm64.zip) | 69 MB | 2026-09-06T22:06Z |
| macos-x86_64 | [macos-x86_64.zip](macos-x86_64.zip) | 73 MB | 2026-09-06T22:06Z |
| windows | [windows.zip](windows.zip) | 79 MB | 2026-09-06T22:05Z |

macOS comes as two downloads, one per processor: **macos-arm64** for Apple Silicon, which is every Mac from late 2020 onwards, and **macos-x86_64** for an Intel Mac. If you are not sure, the Apple menu, then About This Mac, names the chip.

Check a download against what was built:

```
8afafbca8ef0e81ece14f6bb23dd73969c543e51818ef7d592c7846203176443  linux.zip
0d687726735ff33d953bf96de825284aefb22cc7191c91680617679603e61b2c  macos-arm64.zip
ba4d81641daf00dac54ceeea19487293ae0af37d7b77deac19b4bfa2e4e52bc3  macos-x86_64.zip
b9acd8f43e9f5954d7613a23056d228ca5d8f881adf5a5229ec05916b1e23a5a  windows.zip
```

## What is in these builds

| Platform | Version | Engine | Access | Channel | Relay | API | Built-in deck |
| --- | --- | --- | --- | --- | --- | --- | --- |
| linux | 0.0.2 | 4.7.2.stable.mono.arch_linux.ed1daf0bf | restricted | ALPHA | hosted | default | false |
| macos-arm64 | 0.0.2 | 4.7.2.stable.mono.arch_linux.ed1daf0bf | restricted | ALPHA | hosted | default | false |
| macos-x86_64 | 0.0.2 | 4.7.2.stable.mono.arch_linux.ed1daf0bf | restricted | ALPHA | hosted | default | false |
| windows | 0.0.2 | 4.7.2.stable.mono.arch_linux.ed1daf0bf | restricted | ALPHA | hosted | default | false |

What changed in each version is in [CHANGELOG.md](CHANGELOG.md). The version a build is stamped with is also written in the corner of its main menu, next to the commit it came from.

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

Keep the .pck file next to the binary. The game will not start without it.

Nothing needs installing. The .NET runtime is inside the pack.


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

Keep the .pck file next to the .exe. The game will not start without it.

Nothing needs installing. The .NET runtime is inside the pack.


What you need to play
---------------------

An account at https://tcgs.io?game=universus, and a deck of your own. Card art
is fetched as you go, so the first run wants an internet connection.
```

## Copyright

These builds ship no UniVersus artwork: card images are fetched from tcgs.io as they are shown.

UniVersus, and any and all material belonging to it, is copyright UVS Games. No ownership of it is claimed here. This is an unofficial client, and is not affiliated with, endorsed by or sponsored by UVS Games.
