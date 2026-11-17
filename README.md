# Folio public beta

A local-first book and comic reader. This repository distributes beta binaries and collects feedback. Application source is maintained privately.

## Download beta 0.1.0-beta.7

- [Windows x64 portable app](https://github.com/JPClow3/folio-beta/releases/download/v0.1.0-beta.7/Folio-0.1.0-beta.7-windows-x64.exe)
- [Android ARM64 APK — most phones](https://github.com/JPClow3/folio-beta/releases/download/v0.1.0-beta.7/Folio-0.1.0-beta.7-android-arm64-debug.apk)
- [Android x86_64 APK — emulator](https://github.com/JPClow3/folio-beta/releases/download/v0.1.0-beta.7/Folio-0.1.0-beta.7-android-x86_64-debug.apk)
- [Linux x64 .deb](https://github.com/JPClow3/folio-beta/releases/download/v0.1.0-beta.7/Folio-0.1.0-beta.7-linux-amd64.deb)
- [Linux x64 AppImage](https://github.com/JPClow3/folio-beta/releases/download/v0.1.0-beta.7/Folio-0.1.0-beta.7-linux-amd64.AppImage)
- [SHA-256 checksums](https://github.com/JPClow3/folio-beta/releases/download/v0.1.0-beta.7/SHA256SUMS.txt) · [Build manifest](https://github.com/JPClow3/folio-beta/releases/download/v0.1.0-beta.7/manifest.json)

Windows needs WebView2; the portable executable is unsigned. Android APKs are debug signed for sideloading and require Android 7 or later. They use a separate Folio Beta identity and library, so your existing Folio installation is not replaced. Export/import a Folio backup if you want to transfer a library.

Linux packages are unsigned WebKitGTK builds (.deb and AppImage) for amd64. Install the .deb on Debian/Ubuntu-family systems, or mark the AppImage executable and run it. WebKitGTK 4.1 libraries must be available on the host.

Validation of these exact downloads:

- Folio-0.1.0-beta.7-android-arm64-debug.apk: ARM64 build, ABI, signature and embedded asset checks only; no physical phone runtime.
- Folio-0.1.0-beta.7-android-x86_64-debug.apk: android: exact-package runtime checks passed.
- Folio-0.1.0-beta.7-linux-amd64.AppImage: linux: AppImage launch, embedded asset hashes, sample EPUB reading and cold restart on CachyOS.
- Folio-0.1.0-beta.7-linux-amd64.deb: Package integrity checks; runtime unverified for this exact download.
- Folio-0.1.0-beta.7-windows-x64.exe: windows: exact-package runtime checks passed.

iOS builds/widgets remain unverified (no Mac available). Physical Android acceptance, store distribution, Windows signing and store purchases remain outside this beta's validation.

## What to try

Import an EPUB, comic or PDF; read a few pages; close/reopen the app; try airplane mode; resume reading; export and restore a backup. No account or paid subscription is required for local reading. Cloud sync and cloud saving are enabled. Sign in to use the free 500 MB allowance; See Plans & billing for the current paid storage allowance and Premium AI reading tools. From Settings > Account > Cloud sync, use Plans & billing in browser to subscribe or manage billing. Sign in with the same email in the browser, then return to the app and refresh your plan status. Payments use the live provider; completing checkout creates a real paid subscription.

[Report a problem or share feedback](https://github.com/JPClow3/folio-beta/issues/new/choose). Include the beta build, device/OS, file format, steps and expected/actual result. Never include passwords, access keys or private publication files.

## Optional crash and error reports

In **Settings → Advanced → Crash and error reports**, you can opt in to technical failure reports. They start off. Reports contain build, platform, architecture, an error category and hashed app-code locations. They exclude exception messages, publication data, filenames, notes, account details and device identifiers. The receiving service runs on Cloudflare; Cloudflare processes your IP to deliver requests, but Folio does not store it in reports. Collector request logs and traces are disabled.

Turning reports off cancels pending sends and clears saved crash markers. Already sent reports have no device identifier and expire automatically after 30 days (deletion runs asynchronously). Android 11+ can report the category of a previous native crash or ANR after restart; older Android can report Java failures. Native call stacks and desktop minidumps are not collected. Error reports alone cannot establish crash-free users or backend adoption.

The beta feedback form asks which sync option you actually use. All existing backends remain available while feedback is collected; none is being removed based on guesses.

Source commit: `9d36cf5847ce3d7b83792ae9fbd6eb6c775a0783`. Build: `0.1.0-beta.7.9d36cf5847ce` · Offline shell: `fadc750e0d63c1608e277bed`.
