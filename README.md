# Folio public beta

A local-first book and comic reader. This repository distributes beta binaries and collects feedback. Application source is maintained privately.

## Download beta 0.1.0-beta.2

- [Windows x64 portable app](https://github.com/JPClow3/folio-beta/releases/download/v0.1.0-beta.2/Folio-0.1.0-beta.2-windows-x64.exe)
- [Android ARM64 APK — most phones](https://github.com/JPClow3/folio-beta/releases/download/v0.1.0-beta.2/Folio-0.1.0-beta.2-android-arm64-debug.apk)
- [Android x86_64 APK — emulator](https://github.com/JPClow3/folio-beta/releases/download/v0.1.0-beta.2/Folio-0.1.0-beta.2-android-x86_64-debug.apk)
- [SHA-256 checksums](https://github.com/JPClow3/folio-beta/releases/download/v0.1.0-beta.2/SHA256SUMS.txt) · [Build manifest](https://github.com/JPClow3/folio-beta/releases/download/v0.1.0-beta.2/manifest.json)

Windows needs WebView2; the portable executable is unsigned. Android APKs are debug signed for sideloading and require Android 7 or later. They use a separate Folio Beta identity and library, so your existing Folio installation is not replaced. Export/import a Folio backup if you want to transfer a library.

Windows and Android x86_64 have runtime checks. The ARM64 APK also passed reading and offline cold-restart checks on a Samsung Galaxy S24+ (SM-S926B), Android 17. Test publications covered EPUB, CBZ, CBR, CB7 and PDF. This is one phone; readers' own files, the phone's file picker, backup workflows and longer reading sessions still need feedback. iOS, store distribution, Windows signing and store purchases remain outside this beta's validation.

## What to try

Import an EPUB, comic or PDF; read a few pages; close/reopen the app; try airplane mode; resume reading; export and restore a backup. No account or paid subscription is required for local reading. Existing sync/AI features are optional and not the focus of this beta round.

[Report a problem or share feedback](https://github.com/JPClow3/folio-beta/issues/new/choose). Include the beta build, device/OS, file format, steps and expected/actual result. Never include passwords, access keys or private publication files.

## Optional crash and error reports

In **Settings → Privacy → Crash and error reports**, you can opt in to technical failure reports. They start off. Reports contain build, platform, architecture, an error category and hashed app-code locations. They exclude exception messages, publication data, filenames, notes, account details and device identifiers. The receiving service runs on Cloudflare; Cloudflare processes your IP to deliver requests, but Folio does not store it in reports. Collector request logs and traces are disabled.

Turning reports off cancels pending sends and clears saved crash markers. Already sent reports have no device identifier and expire automatically after 30 days (deletion runs asynchronously). Android 11+ can report the category of a previous native crash or ANR after restart; older Android can report Java failures. Native call stacks and desktop minidumps are not collected. Error reports alone cannot establish crash-free users or backend adoption.

The beta feedback form asks which sync option you actually use. All existing backends remain available while feedback is collected; none is being removed based on guesses.

Source commit: `c6a7dc7c64603cc7dc1e2281b4787cd221cc3bdd`. Build: `0.1.0-beta.2.c6a7dc7c6460` · Offline shell: `a224e78ae28c249f788f5673`.
