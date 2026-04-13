# 🚕 Ride-Hailing Ecosystem: Global Architectural Dissection

A high-fidelity, technical encyclopedia mapping the architecture, features, and API ecosystems of the world's leading ride-hailing platforms.

---

### 🏛️ Sanctuary Overview
This repository serves as a private technical archive for the **Database Manager** and **Lead Prototyper**. Each platform and its respective clients have been meticulously probed via APK binary analysis and manifest audit.

*   [**📋 Master Feature Inventory**](./MASTER_FEATURES.md) - Consolidated technical inventory of all identified capabilities.

### 📂 Dissection Index

| Platform | Passenger Report | Driver Report | Key Discoveries |
| :--- | :--- | :--- | :--- |
| **PickMe** | [Passenger](./pickme/passenger/README.md) | [Driver](./pickme/driver/README.md) | CyberSource, GMS GIS, ML Kit Barcodes |
| **Uber** | [Passenger](./uber/passenger/README.md) | [Driver](./uber/driver/README.md) | Braintree/PayPal, Modular UI, Dashboard Auto |
| **Bolt** | [Passenger](./bolt/passenger/README.md) | [Driver](./bolt/driver/README.md) | Mapbox SDK, Veriff Biometrics, Mixpanel |
| **Grab** | [Passenger](./grab/passenger/README.md) | [Driver](./grab/driver/README.md) | Karta Local GIS, Financial Hub, Feature Patching |

---

### 🔍 Research Methodology
1.  **Binary Probing:** Exhaustive string extraction to identify API endpoints and feature flags.
2.  **Manifest Audit:** Full review of Android permissions and service declarations.
3.  **Architectural Mapping:** Visual and technical synthesis of module dependencies.

### 🖼️ Visual Sanctuary
*   [High-Fidelity Architectural Map](./pickme_architecture.svg)

---
*Proprietary Research & Integrity Record | Lead Prototyper: Nimuthu Ganegoda | AI Oversight: Mommy*
