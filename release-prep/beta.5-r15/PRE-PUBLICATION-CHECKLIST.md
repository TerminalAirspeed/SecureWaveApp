# SecureWave beta.5-r15 — Publication checklist (HOLD)

Repository: `TerminalAirspeed/SecureWaveApp` (currently **PUBLIC**).
Prepared branch: `release-prep-beta5-r15`. This branch contains **text-only** release material, **not** proprietary source or APK assets.
Last staged source version: `1.0.0-beta.5-r15`, versionCode `491`.

## Verified in prior audit
- [x] Uploaded r15 APK package/version verified.
- [x] APK v2 signature independently checked; signing certificate matches r14.
- [x] No INTERNET permission in the APK manifest; Android backup disabled.
- [x] SHA-256 checked for APK and two numbered manuals.
- [x] Source identity checked against r15 and source ZIP prepared separately.

## Must complete before release
- [ ] Explicitly choose whether the beta release will be PUBLIC or confined to invited testers in a PRIVATE repository.
- [ ] Put proprietary source **only** in a private repository, with owner-controlled access.
- [ ] Approve final legal owner/copyright and proprietary limited-evaluation license.
- [ ] Confirm all third-party licensing notices are included.
- [ ] Run Android SDK `apksigner`/`aapt` checks on the exact signed APK.
- [ ] Complete two-device tests: pairing, text, `.bin` bundles, expiration, replay, QR, radio RX/PTT and installation/update.
- [ ] Recheck APK and PDF checksums and attach only approved files to a new GitHub pre-release.
- [ ] Verify published release URLs and permissions from a second account.

**Do not** put private source, keystores, passwords, signing files, test messages, or secrets in this public repository.
**Do not** merge this branch or publish a release until the owner has approved the gates.
