# StoneBack  
**From Shop Floor to Field Road.**

StoneBack is an open-source, repairable rear-vision system designed for vehicles that demand long-term reliability, transparency, and serviceability. It combines industrial-grade imaging, embedded computing, and vehicle-hardened electrical design into a fully open platform that can be built, modified, and maintained without proprietary lock-in.

---

## Overview

Modern vehicle camera systems are typically closed, disposable, and dependent on vendor ecosystems. StoneBack is designed as the opposite:

- Fully open hardware and software stack  
- Repairable and upgradeable design  
- No cloud dependency or telemetry  
- Built for decades of service, not product cycles  
- Designed for real-world environments (shops, farms, fleets, RVs)

---

## Full Feature List

### 📷 Vision & Imaging System

- High dynamic range (HDR) real-time imaging pipeline  
- Full-color low-light processing (no infrared grayscale reliance)  
- RAW sensor support (hardware-dependent)  
- Multi-frame temporal noise reduction  
- Lens distortion correction via calibration profiles  
- Adaptive exposure control for harsh lighting environments  

**Viewing Modes**
- Wide-angle safety view (default reverse mode)  
- Dynamic field-of-view scaling  
- Hitch alignment mode for trailers and towing  
- Equipment mode for tractors, industrial vehicles, and RVs  
- Always-on rear view (digital mirror mode optional)

**Environmental Adaptation**
- Rain visibility enhancement mode  
- Snow glare suppression mode  
- Dust and haze clarity mode  
- Night stabilization mode with motion-aware processing  

---

### 🧠 Compute System (StoneBack Core)

- Linux-based embedded compute node (mainline kernel support)  
- ARM-class fanless processor module  
- 4GB RAM baseline (configurable upgrades supported)  
- Replaceable storage (microSD or NVMe options)  
- Hardware video pipeline via deserializer input  
- Deterministic boot (<10 seconds target to video output)

**Operating Modes**
- Appliance Mode (camera-only reliability mode)  
- Node Mode (expandable embedded vehicle computer)

---

### 🔗 Camera Link System

- Serialized video transport over shielded twisted-pair cable  
- Automotive-grade differential signaling  
- 5–10 meter supported cable length  
- EMI-resistant design for vehicle environments  
- Field-repairable, standardized cable system  
- Locking, metal-shell connectors for vibration resistance  

---

### ⚡ Power & Electrical System (Heavy-Duty Design)

- Wide input range: 9V–36V operation  
- Load dump surge protection (alternator disconnect survival)  
- Reverse polarity protection  
- Cold-crank ride-through (no reboot during engine start)  
- Multi-stage EMI filtering  
- Isolated power rails:
  - Compute rail  
  - Camera rail  
  - I/O rail  
  - Standby rail  

Designed for:
- Passenger vehicles  
- Trucks and fleet vehicles  
- Agricultural equipment  
- Industrial and off-grid systems  

---

### 🧰 Hardware Architecture

**Split-System Design**
- Passive rear camera head (no compute, no firmware)  
- Interior-mounted compute node (serviceable and upgradeable)  
- Single-cable connection between modules  

**Camera Head**
- Sealed IP-rated enclosure (IP67/IP69K target)  
- CMOS sensor module  
- Replaceable M12 lens system  
- Serializer-only electronics  
- No software or update surface  

**Compute Node**
- Aluminum passive-cooled chassis  
- Field-replaceable compute/storage  
- Vehicle-mounted protected enclosure  
- Expansion interface support  

---

### 🧪 Calibration System

- Printable calibration target (open standard)  
- Automatic lens distortion mapping  
- Camera height and angle correction  
- Ground-plane distance scaling calibration  
- Vehicle-specific geometry tuning  
- Hitch alignment calibration workflow  

---

### 🧩 Expandability

- Standard internal expansion interface  
- Multi-camera support (future side/rear integration)  
- Optional modules:
  - Trailer camera systems  
  - Side blind-spot cameras  
  - Local recording modules (user-added)  
  - Vehicle telemetry integration (CAN-ready architecture)  

---

### 🔐 Privacy & Security

- No Wi-Fi or Bluetooth required for core operation  
- No cloud services or external dependencies  
- No telemetry or tracking systems  
- Fully offline operation by default  
- Physical ownership equals full system control  
- Optional secure boot (not enforced by default)

---

### 🛠 Serviceability & Longevity

- Fully replaceable camera, cable, and compute components  
- No epoxy-sealed or non-serviceable modules  
- Standard fasteners and connectors throughout  
- Repair documentation included for all subsystems  
- Designed for 10–15+ year operational lifecycle  

---

### 💻 Software Stack

- Mainline Linux OS base  
- V4L2 camera pipeline  
- Open image processing libraries  
- Zero-copy rendering pipeline (where supported)  
- Modular vision processing architecture  

**Vision Pipeline Includes**
- HDR fusion engine  
- Temporal denoise system  
- Lens correction engine  
- Adaptive exposure control  
- Real-time overlay rendering system  

**Output Support**
- HDMI / LVDS display output  
- Reverse trigger GPIO activation  
- Optional always-on display mode  

---

### 🧱 Build Paths

**Performance Build (Reference Design)**
- Serialized camera + full compute pipeline  
- Maximum image fidelity and control  
- Designed for fleets, industrial, and long-term installs  

**Builder Build (Accessible Design)**
- USB/UVC-compatible camera option  
- Simplified installation path  
- Same software stack and feature set where supported  

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
  - [https://roxanneardary.com/stoneback/](https://roxanneardary.com/stoneback/)


## License & Notice Requirements

StoneBack is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.  
- StoneBack specificiations are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.   
  Any update that adds new contributors or modifies attribution should also update `notice.md`.  
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.

---

## Philosophy

StoneBack is built on a simple principle:

> Rear vision is safety-critical infrastructure. It should be open, repairable, and permanent.

This project exists to challenge disposable vehicle electronics and demonstrate that long-life, transparent systems are still possible.

---

## Contributing

Contributions are welcome from engineers, repair technicians, fabricators, and anyone committed to open vehicle systems. Please ensure all contributions align with the licensing and architectural philosophy of the project.
