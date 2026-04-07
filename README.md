# <img src="https://security.kopivo.com/favicon.ico" width="32" height="32" /> # PrivateSecurity: The Ultimate Private Security Suite

![Tech: Web Crypto API](https://img.shields.io/badge/Engine-Web_Crypto_API-blueviolet?style=for-the-badge&logo=webassembly)
![Tech: Client-Side](https://img.shields.io/badge/Powered_by-WebAssembly-654FF0?style=for-the-badge&logo=webassembly)
![Security: 100% Local](https://img.shields.io/badge/Security-100%25_Local-green?style=for-the-badge)
![Architecture: Serverless](https://img.shields.io/badge/Architecture-Serverless-orange?style=for-the-badge)
![Built with: Svelte 5](https://img.shields.io/badge/Built_with-Svelte_5-FF3E00?style=for-the-badge&logo=svelte)

**PrivateSecurity** is a professional-grade, browser-native cryptography and privacy toolkit — and a core pillar of the **Kopivo Suite**. It operates under a strict **Zero-Knowledge architecture**, executing every cryptographic operation directly in the user's browser via the **Web Crypto API** and **WebAssembly**.

> The world's first serverless, privacy-first security suite. No uploads, no servers, 100% local.

### 🌐 [Official Website: security.kopivo.com](https://security.kopivo.com/)

### 🔗 [Part of the Kopivo Ecosystem](https://kopivo.com/)

---

## 📑 Table of Contents

- [The Problem with Cloud Security Tools](#-the-problem-with-cloud-security-tools)
- [How KopivoSecurity Works](#-how-kopivosecurity-works)
- [Available Local Tools](#-available-local-tools--18-modules)
- [Tech Stack](#-tech-stack)
- [Privacy & Security Protocol](#-privacy--security-protocol)
- [The Kopivo Ecosystem](#-the-kopivo-ecosystem)

---

## 🚫 The Problem with Cloud Security Tools

Online security tools that operate server-side create a fundamental paradox: **you are trusting a third party with the very secrets you are trying to protect.**

1. **Key Exposure:** Sending a password, encryption key, or secret phrase to any server — even over HTTPS — creates an interception surface that should never exist.
2. **Metadata Leakage:** File-based cloud tools read your document's metadata, filenames, and content patterns before you ever see the output.
3. **False Anonymity:** "No-log" policies are unverifiable claims. Any server that processes your data *can* retain it.
4. **Behavioral Profiling:** Repeated use of cloud crypto tools creates a behavioral fingerprint — who encrypts what, when, and how often.

**KopivoSecurity eliminates the server, eliminating every one of these risks.**

---

## ⚙️ How KopivoSecurity Works

KopivoSecurity runs every cryptographic and privacy operation natively inside the browser using the **Web Crypto API**, **SubtleCrypto**, and targeted **WebAssembly** modules — with zero server involvement.

- **Web Crypto API Engine:** The browser's built-in, hardware-accelerated cryptographic primitives (AES-GCM, SHA-256, PBKDF2, and more).
- **Edge Execution:** Your CPU and browser sandbox handle all key generation, hashing, and file transformation.
- **Data Sovereignty:** Your keys, messages, and files never leave your device's RAM. Only static assets (HTML/JS/WASM) are served by our CDN.
- **Zero-Footprint:** When the tab closes, all cryptographic material is automatically wiped from volatile memory.
- **Svelte 5 + Runes:** The UI is built with Svelte 5's reactivity system (Runes), delivering a fast, lightweight, zero-overhead interface.

---

## 🛠️ Available Local Tools — 18 Modules

### 🔑 Criptografía y Claves — 5 modules

| Tool | Description |
|---|---|
| **Encrypt Message** | Encrypt and decrypt text messages using AES-256-GCM. No key ever leaves the browser. |
| **Generate Key** | Generate cryptographically secure random keys of any length and encoding (Base64, Hex). |
| **Generate Key** | Build strong, human-readable passphrases using entropy-based wordlist generation. |
| **2FA Generator** | Generate TOTP-compatible 2FA secrets and QR codes for use with any authenticator app. |
| **Base64 Converter** | Encode and decode text, files, or binary data to and from Base64 format. |

### 🗂️ Privacidad de Archivos — 4 modules

| Tool | Description |
|---|---|
| **Encrypt File** | Encrypt any file with a passphrase using AES-256. The output is a portable, encrypted blob. |
| **Clear Image** | Strip all EXIF metadata — GPS, device info, timestamps — from image files before sharing. |
| **Hide in Image** | Embed hidden text or data inside image files using LSB steganography. |
| **Destroy File** | Overwrite file contents with random data before deletion to prevent forensic recovery. |

### 🔍 Seguridad y Auditoría — 5 modules

| Tool | Description |
|---|---|
| **See Metadata** | Inspect the full metadata payload of any file — EXIF, ID3, document properties, and more. |
| **Audit Key** | Analyze password and key strength: entropy, character distribution, and crack-time estimate. |
| **Generate Hash** | Compute cryptographic hashes (MD5, SHA-1, SHA-256, SHA-512) for any file or text string. |
| **Validate Hash** | Verify file integrity by comparing its computed hash against a known reference value. |
| **Clear Link** | Strip tracking parameters (UTM, fbclid, gclid, etc.) from any URL before sharing. |

### 👤 Identidad y Rastreo — 4 modules

| Tool | Description |
|---|---|
| **Fake Profile** | Generate complete synthetic identities (name, address, DOC, email) for testing and privacy. |
| **Browser Footprint** | Reveal your full browser fingerprint — entropy, uniqueness score, and exposed signals. |
| **IP/VPN Leak** | Detect real IP leaks via WebRTC, DNS, and IPv6 — even through active VPN connections. |
| **Adblock Test** | Audit which tracking scripts, ad networks, and telemetry beacons your browser is blocking. |

---

## 🧰 Tech Stack

| Layer | Technology |
|---|---|
| **UI Framework** | Svelte 5 (Runes reactivity system) |
| **Crypto Engine** | Web Crypto API (SubtleCrypto — AES-GCM, SHA-2, PBKDF2, ECDH) |
| **Runtime** | WebAssembly (WASM) for steganography and file-level operations |
| **Entropy Source** | `crypto.getRandomValues()` — CSPRNG native to every modern browser |
| **File I/O** | Browser File API + Blob URL download |
| **Styling** | Scoped Svelte styles + CSS custom properties |
| **Distribution** | Static CDN — zero backend, zero database |

---

## 🛡️ Privacy & Security Protocol

KopivoSecurity operates on a **No-Log, No-Cloud** mandate across all 18 tools:

1. **Local Intake:** Files, keys, and messages are accessed exclusively via the browser's native File API and DOM. No data is ever transmitted.
2. **In-Memory Processing:** All cryptographic operations execute inside a secure, sandboxed Web Worker using SubtleCrypto. The main thread only receives the final output blob.
3. **Instant Output:** The browser triggers a local Blob URL download. **No data is ever sent to a backend.**
4. **No Key Escrow:** KopivoSecurity never stores, logs, or has access to any key, passphrase, or secret generated or used within the suite.
5. **Metadata Awareness:** Unlike cloud tools, KopivoSecurity actively surfaces and strips metadata — it never reads it for profiling.

---

## 🔗 The Kopivo Ecosystem

KopivoSecurity is one pillar of the broader **Kopivo** privacy-first productivity suite:

| Product | Focus | URL |
|---|---|---|
| **Kopivo PDF** | PDF management & editing | [pdf.kopivo.com](https://pdf.kopivo.com/) |
| **Kopivo Media** | Video & audio processing | [media.kopivo.com](https://media.kopivo.com/) |
| **Kopivo Security** | Cryptography & privacy tools | [security.kopivo.com](https://security.kopivo.com/) |
| **Kopivo Devs** | Developer toolkit | [dev.kopivo.com](https://dev.kopivo.com/)
---

## 💬 Support & Contribution

KopivoSecurity is built to make the web private again — one secret at a time.

1. **Star this Repo:** Help security professionals, journalists, and privacy advocates find a trustworthy local alternative.
2. **Spread the Word:** Share with developers, activists, lawyers, and anyone handling sensitive data.
3. **Feedback:** Reach out via [security.kopivo.com](https://security.kopivo.com/) for feature requests or technical inquiries.

---

*Precision. Privacy. Performance. © 2026 Kopivo.*
