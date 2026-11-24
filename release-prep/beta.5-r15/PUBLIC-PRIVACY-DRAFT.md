# SecureWave public beta — Privacy statement (DRAFT)

SecureWave's verified r15 APK does not request Android `INTERNET` permission and has Android backups disabled. SecureWave performs supported cryptographic operations on-device. Its user-controlled external share destinations and transport apps are separate applications with their own permissions, networks and policies.

SecureWave locally handles contacts, encrypted messages and attachments, cryptographic keys, pairing records, replay/receipt records, preferences and expiration state. App-level deletion cannot guarantee erasure of material already sent to other applications, received by another person, backed up externally or otherwise copied.

Camera access supports QR workflows. Microphone/audio and foreground service permissions support radio operation; notification permissions support status updates. The signed APK manifest and actual runtime behavior, rather than this document alone, determine permissions.

Filename randomization and supported image metadata handling reduce certain disclosures but do not guarantee complete metadata removal. External sharing can disclose participants, timestamps and payload sizes even though content is encrypted. Link tracking parameters are not automatically removed by r15.

This statement is a draft for the owner's review. It is not an independent security certification. Do not share confidential contacts, QR secrets, keys, logs or message content in public issues.
