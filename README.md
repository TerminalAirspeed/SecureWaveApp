# SecureWave

**SecureWave is a Android application for secure, user-controlled communications and encrypted local files.**

**SecureWave** is a privacy-focused Android application designed for secure communication and encrypted file storage. It combines end-to-end encrypted text messaging, secure file exchange, verified contact pairing, and encrypted /unencrypted radio communications in one application. Built with security and user control in mind, SecureWave operates without direct internet access, allowing users to communicate through external messaging applications or compatible radio equipment while keeping sensitive information protected.


**SecureWave has NO INTERNET access**


**SecureWave is currently in beta testing and is under active development.** User feedback is greatly appreciated and will help guide future improvements. I welcome suggestions for new features, usability enhancements, performance improvements, and any bugs or issues encountered. Your input will help make SecureWave more secure, reliable, and user-friendly.
>
>
> **SHA-256 checksum for SecureWave 1.0.0-beta.5-r15 APK is: a3f571b9f9e9df70813f958154e0569842525eb23b2f0a3f424042fea84e9010**

## SecureWave screenshots

The screenshots below are from the SecureWave project. They are **real application screenshots**, not mockups or AI-generated illustrations. They may represent an earlier build and are shown for orientation; the exact interface can change between releases.

### Main screen and secure messaging

| SecureWave Home | Secure Text |
|:---:|:---:|
| ![Actual SecureWave Home screenshot](https://raw.githubusercontent.com/TerminalAirspeed/SecureWaveApp/release-prep-beta5-r15/screenshots/securewave-home.png) | ![Actual SecureWave Secure Text screenshot](https://raw.githubusercontent.com/TerminalAirspeed/SecureWaveApp/release-prep-beta5-r15/screenshots/secure-text.png) |

### Secure Files and encrypted radio

| Secure Files | Secure Radio |
|:---:|:---:|
| ![Actual SecureWave Secure Files screenshot](https://raw.githubusercontent.com/TerminalAirspeed/SecureWaveApp/release-prep-beta5-r15/screenshots/secure-files.png) | ![Actual SecureWave Secure Radio screenshot](https://raw.githubusercontent.com/TerminalAirspeed/SecureWaveApp/release-prep-beta5-r15/screenshots/secure-radio.png) |

### Open Radio and radio hardware setup

| Open Radio — unencrypted | Radio hardware setup |
|:---:|:---:|
| ![Actual SecureWave Open Radio screenshot](https://raw.githubusercontent.com/TerminalAirspeed/SecureWaveApp/release-prep-beta5-r15/screenshots/open-radio.png) | ![SecureWave radio equipment setup image](https://raw.githubusercontent.com/TerminalAirspeed/SecureWaveApp/release-prep-beta5-r15/screenshots/securewave-radio-setup.jpg) |


## Capabilities

- **Secure Text:** Prepare authenticated encrypted text for user-selected external transport.
- **Secure pairing:** Contact and key-verification workflows for establishing trusted keys.
- **Secure Files:** Encrypted local storage and exchange of protected attachments or file bundles.
- **Secure Radio:** Encrypted radio/audio messaging using compatible equipment and authorized frequencies.
- **Open Radio:** Unencrypted radio communication; **not** a confidential channel.
- **Local-first design:** SecureWave does not request Android's `INTERNET` permission.
  
**SecureWave Encryption**

SecureWave uses advanced cryptographic technologies to protect messages, files, and radio communications. It combines AES-256 authenticated encryption with hybrid secure pairing using elliptic-curve cryptography (P-256) and post-quantum ML-KEM-768 key establishment. Additional safeguards include contact verification, replay protection, and encrypted local storage. Encryption and decryption take place directly on the user's device, helping keep sensitive information private and under the user's control. SecureWave's Open Radio mode is intentionally unencrypted.


## Downloads and installation

Official APK releases, when available, will be published here:

**[SecureWave GitHub Releases](https://github.com/TerminalAirspeed/SecureWaveApp/releases)**

1. Download an APK **only from the official releases page**.
2. Check its SHA-256 hash against the checksum published with that release.
3. On an Android device, allow installation from your chosen file manager or browser only when prompted and only if you trust the package.


The intended upcoming beta targets **Android 10 (API 29) or newer**, subject to verification of the final release APK.

## Privacy and security boundaries

- SecureWave's application process is designed for offline/local operation. **No `INTERNET` permission** is requested by the audited beta build.
- Disappearing messages cannot guarantee removal from external applications, screenshots, backups or recipient-controlled devices.
- The application has **not received an independent security audit or certification**. Do not rely on a beta for emergencies, life safety or mission-critical secrecy.
- **Open Radio is unencrypted.** Use of encryption over radio is subject to service-specific rules. Encrypted transmissions generally are prohibited on U.S. amateur-radio and GMRS services.

## Licensing and source code

SecureWave is **free to use** when distributed through authorized official channels.

The final owner-approved license and all required third-party notices will accompany an approved public release. This README is not a substitute for those documents.

## Feedback and responsible disclosure

Use [GitHub Issues](https://github.com/TerminalAirspeed/SecureWaveApp/issues) for **non-sensitive** bug reports. Do not publish passwords, cryptographic keys, pairing codes, private messages, personal contacts or unredacted logs. Security vulnerabilities should be reported privately using GitHub's private vulnerability reporting if enabled.

---

**SecureWave** · Proprietary Android software · Public documentation and approved APK distribution only
