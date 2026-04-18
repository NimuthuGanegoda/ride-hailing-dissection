# 📱 Bolt Passenger: High-Fidelity Dissection Report

![Platform](https://img.shields.io/badge/Platform-Bolt-35D07F?style=for-the-badge&logo=bolt&logoColor=white)
![Tech](https://img.shields.io/badge/Tech-Android%20(APK)-3DDC84?style=for-the-badge&logo=android&logoColor=white)
![Status](https://img.shields.io/badge/Status-Dissected-green?style=for-the-badge)

A technical audit of the **Bolt Passenger** application, focusing on European-market GIS implementations and biometric identity verification.

---

### 📂 Feature Dissections
For granular technical reports, see the individual feature files:
*   [🗺️ GIS & Route Optimization](features/mapping.md)
*   [🛡️ Identity & Verification](features/identity.md)
*   [🚗 Core Mobility & Dispatch](features/dispatch.md)
*   [🧩 Advanced Architecture](features/architecture.md)

---

### 🔍 Metadata & Identification
*   **📦 Package Name:** `ee.mtakso.client`
*   **🏗️ Architecture Support:** `armeabi-v7a` (v118 MB base)
*   **🎯 Target SDK:** 35 (Android 15)

> [!NOTE]
> Bolt heavily utilizes **Veriff** for automated biometric identity verification across its European operations.

---
*Proprietary Dissection Record | Lead Developer: Nimuthu Ganegoda | Architectural Prototyper*

