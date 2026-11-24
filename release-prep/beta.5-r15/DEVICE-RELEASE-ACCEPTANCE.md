# SecureWave r15 signed APK — Two-device acceptance record

**Release:** 1.0.0-beta.5-r15 / versionCode 491  
**APK SHA-256:** `a3f571b9f9e9df70813f958154e0569842525eb23b2f0a3f424042fea84e9010`  
**State:** NOT YET ATTESTED AS TESTED. Fill in actual outcomes; do not mark PASS based only on source inspection.

| Test | Result | Evidence / notes |
|---|---|---|
| Install signed r15 over r14 without uninstall, preserve vault/keys | NOT RUN | |
| Fresh signed r15 install on second device | NOT RUN | |
| Hybrid P-256 + ML-KEM-768 pairing with 20-digit verification | NOT RUN | |
| Mismatched verification rejects pairing | NOT RUN | |
| Current-format encrypted text both directions | NOT RUN | |
| Current-format rejection of obsolete/invalid messages | NOT RUN | |
| Replay of authenticated text/file/radio payload rejected after restart | NOT RUN | |
| Prepared attachment cannot send without SEND | NOT RUN | |
| Mixed `.bin` bundle send/receive, verify and open | NOT RUN | |
| Randomized recipient-visible filenames and optional original name | NOT RUN | |
| Secure Files saved/opened; full-screen image zoom | NOT RUN | |
| Disappearing text/file timer, unopened 30-day limit and tombstone | NOT RUN | |
| Manual key QR and offline QR scanner; permission behavior | NOT RUN | |
| Preferred Sharesheet sending app and external-app handoff | NOT RUN | |
| Secure Radio audio RX/TX, PTT and OFDM with real hardware | NOT RUN | |
| Open Radio clearly unencrypted; radio regulatory notice understood | NOT RUN | |
| App Lock, background behavior, screen lock and Secure Clear | NOT RUN | |
| No unexpected network permission or exported components | VERIFIED BY PREVIOUS APK AUDIT | |
| Official Android SDK `apksigner verify --verbose --print-certs` | NOT RUN | Android SDK missing in inspection environment |

Tester device models, Android versions, run date and signature of test owner: **TO BE RECORDED**.

Any failed security-critical test blocks public beta publication until corrected or risk accepted explicitly and transparently.
