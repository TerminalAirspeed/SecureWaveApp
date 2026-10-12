[README(1).md](https://github.com/user-attachments/files/33353218/README.1.md)

# SecureWave

**Private messaging and digital radio messaging for Android.**

**PUBLIC BETA** · Android 10+ · APK download only

> [!IMPORTANT]
> **SecureWave does not request Internet access and does not collect information for its developer.** There is **no Android `INTERNET` permission**, no SecureWave account, no advertising, no analytics or tracking SDK, and no automatic usage, diagnostic, or crash-report upload. SecureWave does not transmit your contacts, messages, files, keys, device identifiers, or activity to a SecureWave server. See [Privacy](#privacy-no-internet-permission-no-developer-data-collection) for what the app handles locally and what changes when you choose an external transport.
>
> **PUBLIC BETA:** SecureWave is undergoing field testing and has **not been independently security-audited or certified**. Do not rely on it as your only means of emergency communication. Encrypted radio transmission is not legal on every frequency or radio service; see [Radio regulations](#radio-regulations).

## Download and install

**[Get the SecureWave APK from GitHub Releases](../../releases)**

This repository currently distributes **compiled Android APKs only**. The application source code is **not being published at this stage**. Each public release should provide the APK, its version, and release notes; GitHub automatically displays a SHA-256 digest for each uploaded release asset. Download only from this repository's Releases page.

1. Open **Releases** and select the newest **Public Beta** release.
2. Download its `.apk` file. Compare the downloaded APK with the SHA-256 shown next to its release asset before installing.
3. Open the APK on your Android device. If prompted, allow your browser or file manager to **install unknown apps** for this installation.
4. Launch SecureWave and grant permissions only for features you intend to use. Microphone access is necessary for radio audio; notifications may be needed for foreground radio reception.
5. Create a contact and test a short message before relying on SecureWave for regular communication.

**Updates:** Install a newer official APK over the existing installation to preserve app data, provided it uses the same application ID and signing certificate. **Do not uninstall SecureWave just to upgrade**—uninstalling can erase its contacts, protected keys, and stored content. GitHub APK releases do not update automatically through the Play Store.


## What SecureWave does

SecureWave performs supported encryption and decryption **on the Android device**. It combines several tools in one application:

| Feature | Description |
| --- | --- |
| **Secure Text** | Create and read contact-specific, authenticated encrypted messages. Hand off the encrypted payload through a messaging or sharing app you choose; the recipient explicitly imports the payload. |
| **Secure Files** | Keep files in an encrypted local vault and exchange authenticated encrypted file payloads with a contact. |
| **Secure Radio** | Transmit encrypted **digital messages/data** as modem audio through compatible external radio and audio equipment. This can be automated with Digirig Lite and associated cables. |
| **Open Radio** | A separate radio mode for **unencrypted** communication. This can be automated with Digirig Lite and associated cables. **Do not use this mode for confidential information.** |
| **Contacts** | Search names, mark Favorites, identify the selected recipient, and view contact security status. |

### Security features

- **Hybrid Secure Pairing:** P-256 + ML-KEM key establishment with a verification code that users must compare through a trusted channel.
- **Fast Radio Pairing:** P-256-based pairing for radio use; **not post-quantum**.
- **Manual-key contacts:** Generate or enter a shared 32-character secret; manual groups are also supported.
- **Device protection:** Android Keystore-backed protection where supported, encrypted local storage, optional App Lock, screenshot restrictions on protected screens, controlled clipboard handling, and deliberate **Secure Clear** actions.
- **Radio controls:** Manual PTT, selected supported automatic-PTT arrangements, and foreground receive operation, subject to Android and hardware limitations.

> **Important:** SecureWave is not itself an Internet messenger or a Signal/Molly client. It does not automatically deliver Secure Text over a network. If you choose another app to carry encrypted payloads, that app has its own permissions, retention practices, and metadata exposure.

## Requirements

- **Android:** Version 10 (API 29) or newer.
- **For Secure Text/Files:** A second person using a compatible SecureWave protocol version and an appropriate way to exchange encrypted payloads.
- **For radio:** A compatible radio, audio interface/cabling, correctly routed audio, and a tested PTT method. Not all USB/audio or automatic-PTT hardware is supported.
- **For encrypted radio transmission:** Appropriate authorization for the specific radio service, frequency, emission type, equipment, and station.

## Basic use

1. **Create or select a contact.** When securely pairing, compare the *entire* verification code with your contact before accepting trust.
2. **Choose a mode.** Use **Secure Text** for encrypted messages, **Secure Files** for encrypted storage and file exchange, or **Secure Radio** with compatible hardware and legal transmit authorization.
3. **Confirm the recipient and send.** The content stays protected by SecureWave's application-layer encryption, but transport and delivery remain separate responsibilities.
4. **Verify receipt.** Outside messaging apps and radio links can delay, lose, or retain ciphertext. Secure Radio operates half-duplex and does not guarantee acknowledgement or delivery.

A copied manual key is a **secret**, even if SecureWave marks clipboard data sensitive and attempts to clear it promptly. Exchange manual keys through a trusted channel; avoid chat backups, clipboard-history services, and unintended recipients.

## Privacy: no Internet permission, no developer data collection

**SecureWave does not request Android's `INTERNET` permission. It does not collect or send personal information, telemetry, analytics, or usage data to the SecureWave developer.** No account, login, cloud account, proprietary server, advertising identifier, analytics SDK, or automatic crash-reporting service is required or used by the app.

- **No information is collected remotely by SecureWave:** The developer receives no contacts, conversations, files, radio traffic, encryption keys, device identifiers, location, or usage reports from the app.
- **Information processed locally is not the same as developer data collection:** SecureWave needs to access information you choose to enter or import. It may store your contacts, encrypted history, vault files, settings, and security state **on your device** so the requested features work. It also uses microphone/audio input when you enable radio functionality.
- **No automatic Internet delivery:** Secure Text and encrypted file payloads leave SecureWave only through user-initiated export/share or radio transmission. If you choose a separate messaging, email, or file-sharing application to carry ciphertext, that third-party application may use the Internet and may collect transport metadata under **its own** privacy practices.
- **External services are separate:** GitHub may record website visits or APK downloads, and information you voluntarily submit through GitHub Issues or other feedback channels goes to that service. That is separate from SecureWave app telemetry.

**In short: SecureWave protects and processes your information locally; it does not collect it for the developer or send it to a SecureWave server.**

## Security limitations

SecureWave is designed around authenticated encryption and local protection.

- **Verify identities.** A pairing process is not trusted until both parties compare the complete verification code.
- **Shared groups do not authenticate individual senders.** Anyone holding a manual group key may claim a sender name.
- **Protect your endpoints.** A compromised device, malicious keyboard, exposed clipboard, unlocked screen, or exported plaintext can expose sensitive content.
- **Transport metadata remains visible to transport providers.** SecureWave encrypts message contents, not necessarily who exchanges payloads, when, or through which outside app or radio system.
- **Secure Clear is destructive.** It is intended to remove protected application state and may make prior content unrecoverable.
- **Testing is ongoing.** Current beta testing does not replace independent cryptographic review, penetration testing, and wider device/hardware qualification.

## Radio regulations

**You are responsible for following all applicable radio laws and license conditions.** Owning a radio—or having a channel labeled *business*—does not automatically authorize digital or encrypted transmission.

In the United States:

- **Amateur Radio (FCC Part 97):** Messages encoded to obscure their meaning are generally prohibited under [47 CFR § 97.113(a)(4)](https://www.ecfr.gov/current/title-47/chapter-I/subchapter-D/part-97/section-97.113). **Do not transmit SecureWave encrypted traffic on amateur-radio frequencies.**
- **Industrial/Business Radio (FCC Part 90):** Scrambling and certain digital emissions may be permitted **only within the applicable station authorization and technical/service rules**. Encrypted data transmissions also require appropriate data-emission authorization; see [47 CFR § 90.212](https://www.ecfr.gov/current/title-47/chapter-I/subchapter-D/part-90/section-90.212).
- **GMRS (FCC Part 95):** Messages with concealed meanings are prohibited under [47 CFR § 95.1733](https://www.ecfr.gov/current/title-47/chapter-I/subchapter-D/part-95/section-95.1733). **Do not transmit SecureWave encrypted traffic on GMRS.**

Other countries have different requirements. Check the rules for **your actual station and equipment** before transmitting. SecureWave does not determine whether your use is lawful.

## Beta feedback and security reports

Please use this repository's **Issues** area (if enabled) to report non-sensitive bugs and usability feedback. Include the SecureWave version, Android version, hardware/audio interface if relevant, reproduction steps, and observed behavior.

**Do not post encryption keys, pairing secrets, personal messages, unredacted protected screenshots, or sensitive diagnostics in public Issues.** For a potential security vulnerability, use GitHub's **private vulnerability reporting** if enabled, or contact the maintainer privately through the project's designated security channel.

## Distribution and third-party licenses

This GitHub repository currently provides the **application APK, not the SecureWave source code**. Availability of an APK does not itself grant a license to modify or redistribute SecureWave.

SecureWave uses third-party software, including **Bouncy Castle Java**. Bouncy Castle is distributed under a permissive MIT-style license, which requires preservation of its copyright and permission notice. The notice is reproduced here; this does **not** represent a complete review of every release dependency.

<details>
<summary>Bouncy Castle Java copyright and permission notice</summary>

Copyright (c) 2000–2026 The Legion of the Bouncy Castle Inc. (https://www.bouncycastle.org)

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Source: [Bouncy Castle Java license](https://github.com/bcgit/bc-java/blob/main/LICENSE.md).

</details>

**Release maintainers:** Confirm that all required third-party notices are included with the distributed APK or release materials before publishing. An APK-only release does not waive open-source license obligations.

---

*SecureWave is an independent application and is not affiliated with Signal, Molly, or any radio manufacturer. Features and supported hardware may change during public beta.*
