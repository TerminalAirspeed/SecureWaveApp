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

## Cleanup performed
- [x] Removed obsolete beta.3 manuals and screenshots from the public default branch.
- [x] Replaced the stale default-branch README with a release-preparation notice.
- [x] Owner deleted the **public beta.3 GitHub Release**. Verified release list is empty on November 24, 2026.
- [ ] Old `v1.0.0-beta.3` **tag still exists**. Remove via GitHub Tags if desired; commit history may persist.

## Must complete before release
- [x] Owner selected the existing PUBLIC `TerminalAirspeed/SecureWaveApp` repository for APK downloads; the proprietary Android Studio source remains PRIVATE.
- [ ] Put proprietary source **only** in a private repository, with owner-controlled access.
- [ ] Approve final legal owner/copyright and proprietary limited-evaluation license. Draft terms staged under this directory, **not approved**.
- [ ] Confirm complete third-party licensing notices accompany the final signed APK release (Bouncy Castle and ZXing).
- [ ] Run Android SDK `apksigner`/`aapt` checks on the exact signed APK.
- [ ] Complete and sign the staged DEVICE-RELEASE-ACCEPTANCE.md two-device testing report (pairing, text, `.bin`, expiration, replay, QR, radio RX/PTT and installation/update).
- [ ] Recheck APK and PDF checksums and attach only approved files to a new GitHub pre-release.
- [ ] Verify published release URLs and permissions from a second account.

**Do not** put private source, keystores, passwords, signing files, test messages, or secrets in this public repository.
**Do not** merge this branch or publish a release until the owner has approved the gates.
