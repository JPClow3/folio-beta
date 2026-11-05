# Folio public beta

A local-first book and comic reader. This repository distributes beta binaries and collects feedback. Application source is maintained privately.

## Download beta 0.1.0-beta.4

- [Windows x64 portable app](https://github.com/JPClow3/folio-beta/releases/download/v0.1.0-beta.4/Folio-0.1.0-beta.4-windows-x64.exe)
- [Android ARM64 APK — most phones](https://github.com/JPClow3/folio-beta/releases/download/v0.1.0-beta.4/Folio-0.1.0-beta.4-android-arm64-debug.apk)
- [Android x86_64 APK — emulator](https://github.com/JPClow3/folio-beta/releases/download/v0.1.0-beta.4/Folio-0.1.0-beta.4-android-x86_64-debug.apk)
- [SHA-256 checksums](https://github.com/JPClow3/folio-beta/releases/download/v0.1.0-beta.4/SHA256SUMS.txt) · [Build manifest](https://github.com/JPClow3/folio-beta/releases/download/v0.1.0-beta.4/manifest.json)

Windows needs WebView2; the portable executable is unsigned. Android APKs are debug signed for sideloading and require Android 7 or later. They use a separate Folio Beta identity and library, so your existing Folio installation is not replaced. Export/import a Folio backup if you want to transfer a library.

Windows and Android x86_64 have runtime checks. ARM64 is compiled and structurally checked; testing on physical phones is the next priority. iOS, store distribution, Windows signing and store purchases remain outside this beta's validation.

## What to try

Import an EPUB, comic or PDF; read a few pages; close/reopen the app; try airplane mode; resume reading; export and restore a backup. No account or paid subscription is required for local reading. Cloud sync and cloud saving are enabled. Sign in to use the free 500 MB allowance; Pro offers 10 GB, and Premium adds AI reading tools. From Settings > Sync & backup > Cloud sync, use Plans & billing in browser to subscribe or manage billing. Sign in with the same email in the browser, then return to the app and refresh your plan status. Payments use the live provider; completing checkout creates a real paid subscription.

[Report a problem or share feedback](https://github.com/JPClow3/folio-beta/issues/new/choose). Include the beta build, device/OS, file format, steps and expected/actual result. Never include passwords, access keys or private publication files.

## Optional crash and error reports

In **Settings → About & diagnostics → Crash and error reports**, you can opt in to technical failure reports. They start off. Reports contain build, platform, architecture, an error category and hashed app-code locations. They exclude exception messages, publication data, filenames, notes, account details and device identifiers. The receiving service runs on Cloudflare; Cloudflare processes your IP to deliver requests, but Folio does not store it in reports. Collector request logs and traces are disabled.

Turning reports off cancels pending sends and clears saved crash markers. Already sent reports have no device identifier and expire automatically after 30 days (deletion runs asynchronously). Android 11+ can report the category of a previous native crash or ANR after restart; older Android can report Java failures. Native call stacks and desktop minidumps are not collected. Error reports alone cannot establish crash-free users or backend adoption.

The beta feedback form asks which sync option you actually use. All existing backends remain available while feedback is collected; none is being removed based on guesses.

Source commit: `9af68a7fd55eceef08eccbbf56769747fd951b44`. Build: `0.1.0-beta.4.9af68a7fd55e` · Offline shell: `16ff888d28cbd79ea67cebb0`.
