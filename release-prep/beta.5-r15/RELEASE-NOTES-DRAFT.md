# SecureWave 1.0.0-beta.5-r15 — Release Candidate (DRAFT)

> **DO NOT PUBLISH YET.** This is a staging document, not an approved release. The current public download remains beta.3.

**Version:** 1.0.0-beta.5-r15 · **versionCode:** 491 · **Android:** 10+ (API 29+) · **Package:** `com.securewave.alpha32`.

## What's new in r15

- Prepared attachment composer with image previews, removable attachments, and a visible **PREPARED — NOT SENT** state.
- Files are not handed to another app until SEND is pressed.
- Randomized recipient-visible filenames are the default; keeping original filenames is optional.
- Android Sharesheet and per-contact preferred sending app are retained.

## Existing features

- Secure Text: authenticated encrypted messages; manual external ciphertext handoff.
- Secure Files: encrypted vault, authenticated mixed-file `.bin` bundles, full-screen image viewing, and secure-folder-first export.
- Disappearing content: first-view expiration; unopened content cap of 30 days.
- Secure Pairing: hybrid P-256 + ML-KEM-768; separate conventional P-256 Fast Radio Pairing.
- Secure Radio: OFDM audio modem, authenticated encryption and replay protection; Open Radio is explicitly unencrypted.
- Offline local operation: SecureWave itself does not request the Android INTERNET permission.

## Security and operational boundaries

SecureWave is a **beta**, has **not** had an independent security audit, and must not be relied upon for emergency communications or the protection of critical information. Use test data. Sending ciphertext to an external app does not prove delivery. External apps have their own privacy and metadata practices. A recipient or malicious device can retain copies despite expiration. Current-only formats mean older versions may be incompatible.

**Radio operation:** Encrypted transmissions are generally not permitted on U.S. amateur frequencies or GMRS. Operators are responsible for the rules of their service, spectrum authorization, equipment and emission.

## Planned release assets (not yet uploaded)

- `SecureWave-1.0.0-beta.5-r15.apk`
- `SecureWave-Quick-Start-beta5-r15-Numbered-Screens.pdf`
- `SecureWave-User-Manual-beta5-r15-Numbered-Screens.pdf`
- `SHA256SUMS.txt`

The SecureWave Android Studio source is **not** part of the public beta-download repository.

## Publication gates

1. Confirm owner-approved **proprietary limited evaluation terms** and third-party notices.
2. Complete official Android SDK APK verification and at least two-phone acceptance tests.
3. Recheck checksum manifest against exact release assets.
4. Confirm desired audience and access policy before making this release visible.

Do not replace older release assets or publish this draft as a release without completing these checks.
