# DrivePass

## The Secure Layer Between You and Go.

DrivePass is an open-source **AGPL-3.0+ vehicle access and control platform** designed to replace traditional key fobs with encrypted, identity-based authentication. Built for retrofit compatibility, it brings secure digital access, remote start, and intelligent vehicle control to both modern and legacy vehicles.

---

## 🚗 Core Features

- Secure lock and unlock via mobile device  
- Encrypted remote start with safety validation  
- Keyless driving authorization system  
- Retrofit compatibility for older vehicles  
- Shareable digital access keys with permissions  
- Offline-first operation (no required cloud dependency)  
- Multi-device support for households and fleets  
- Role-based access control (owner, guest, service, caregiver)  
- Temporary and scheduled access keys  
- Emergency lockout and recovery mode  

---

## 🔐 Security Architecture

DrivePass is built on a zero-trust security model:

- End-to-end encrypted communication channels  
- ECC cryptography with AES-256-GCM transport encryption  
- Hardware root-of-trust using secure elements  
- Rolling challenge–response authentication  
- Mandatory Two-Factor Authentication (2FA) for sensitive actions  
- Biometric confirmation required for ignition authorization  
- Anti-replay and anti-relay attack protection  
- Signed firmware and secure boot enforcement  
- Local-only key storage (no centralized credential dependency)  

---

## 🚗 Remote Start Safety System

Remote start is only executed when all conditions are met:

- Transmission verified in Park/Neutral  
- Brake and hood safety interlocks confirmed  
- Tamper detection passed  
- Cryptographic session validation complete  
- Authorized user identity confirmed via 2FA  

---

## 🧠 Vehicle Intelligence Features

DrivePass extends beyond access control into secure vehicle awareness:

- Presence-aware passive entry and auto-locking  
- Secure drive authorization before gear engagement  
- Local encrypted vehicle diagnostics  
- Battery voltage and power monitoring  
- Door, ignition, and engine state awareness  
- Multi-vehicle management dashboard  
- Family, fleet, and caregiver permission systems  
- Accessibility-focused control modes  

---

## 🤖 AI & Automation Features

DrivePass supports local-first intelligent automation designed for assistance, not surveillance:

- Smart anomaly detection for unusual access behavior  
- Impossible travel and failed authentication pattern detection  
- Adaptive authentication based on risk and location context  
- Intelligent remote-start climate optimization  
- Battery-aware power conservation automation  
- Event-driven automation rules for fleets and households  
- Fully optional AI modules with local execution preference  

---

## 🛠 Retrofit-First Design Philosophy

- Compatible with legacy and modern vehicles  
- Non-invasive installation approach  
- Modular hardware design for scalability  
- Open hardware architecture  
- Repairable and serviceable by design  
- Designed for long-term ownership independence  

---

## 💻 Technology Stack

### Mobile Application
- Flutter (cross-platform iOS + Android)  
- Secure Enclave / Android Keystore integration  
- Offline-first encrypted identity storage  

### Embedded Systems
- Rust-based firmware (memory-safe architecture)  
- ESP32-class microcontrollers  
- BLE, NFC, and optional UWB support  
- Secure boot and signed OTA updates  

### Security Layer
- Hardware root-of-trust  
- Mutual authentication system  
- Perfect Forward Secrecy session keys  
- Open cryptographic standards for auditability  

### AI & Automation Layer
- Local-first inference architecture  
- Event-driven automation engine  
- On-device behavioral analysis  
- Privacy-preserving intelligence system design  

---

## 🌐 Open Source Commitment

DrivePass is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.

---

## Specification Branding License (SBL)

### Standard
- Fully AGPL-3.0+ compliant system
- Copyleft enforced for network deployments
- Required attribution:
  - Roxanne Ardary
  - https://www.roxanneardary.com/

### Optional

- **Specification Branding License (SBL)**
  - Attribution-free commercial deployment
  - Pricing based on scale, usage, and deployment scope
  - [https://roxanneardary.com/drivepass/](https://roxanneardary.com/drivepass/)  

---

## 📌 License & Notice Requirements

DrivePass is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.  
- DrivePass specifications are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.  
  Any update that adds new contributors or modifies attribution should also update `notice.md`. 
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.

---

## 🚘 Vision

DrivePass is built on a simple principle:

**Your vehicle should recognize you — not a corporation.**

Secure.  
Private.  
Repairable.  
Owner-controlled.

#DrivePass  
