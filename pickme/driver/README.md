# 🚛 PickMe Driver: High-Fidelity Dissection Report

![Platform](https://img.shields.io/badge/Platform-PickMe-FFD800?style=for-the-badge&logo=pickme&logoColor=black)
![Tech](https://img.shields.io/badge/Tech-Android%20(APK)-3DDC84?style=for-the-badge&logo=android&logoColor=white)
![Status](https://img.shields.io/badge/Status-Verified-brightgreen?style=for-the-badge)

A rigorous architectural audit of the **PickMe Driver (BYOD)** application, detailing the telemetry, dispatch, and system-level controls used by the platform.

---

### 🔍 Metadata & Identification
*   **📦 Package Name:** `com.pickme.driver.byod`
*   **🔢 Version Name:** `37.3.2L` (v739)
*   **🎯 Target SDK:** 35 (Android 15) | **Min SDK:** 26 (Android 8.0)
*   **🏗️ Architecture Support:** `arm64-v8a` (Configured via split APKs)

---

### 🛠️ Core Permission Profile (System Dominance)
The driver client is designed for total persistence and device control to ensure 100% dispatch reliability:
*   **🛰️ Persistent Tracking:** `ACCESS_BACKGROUND_LOCATION`, `ACCESS_FINE_LOCATION`, `FOREGROUND_SERVICE_LOCATION`.
*   **🖥️ System Overlays:** `SYSTEM_ALERT_WINDOW` (Allows dispatch alerts to appear over any other app).
*   **🔐 Persistence:** `RECEIVE_BOOT_COMPLETED`, `WAKE_LOCK`, `DISABLE_KEYGUARD`, `REQUEST_IGNORE_BATTERY_OPTIMIZATIONS`.
*   **⏰ Scheduling:** `SCHEDULE_EXACT_ALARM` (Ensures critical job alerts are never delayed).

---

### 📍 Architectural Modules
#### 1. 📡 Real-Time Dispatch Engine
*   **⚡ Protocol:** Utilizes high-frequency telemetry ingestion to sync driver status with the central hub.
*   **🧠 Logic:** Managed via `driver-api-go.pickme.lk` for ride-hailing and `delivery-driver-api.pickme.lk` for logistical orchestration.

#### 2. 💬 In-App Communication Hub
*   **🗣️ Chat Server:** Connects to `driver-chat-server.pickme.lk`.
*   **🔌 Technology:** Implements real-time messaging for passenger-driver coordination via WebSockets.

#### 3. 🔐 Verification & Lifecycle
*   **📝 Self-Registration:** Contains a complete portal for driver on-boarding (`driver-mobile-self-registration.pickme.lk`).
*   **🆔 Identity Integrity:** Frequent use of `READ_PHONE_STATE` and `AD_ID` to bind driver accounts to specific physical hardware.

---

### 🚀 Unique Platform Features
*   **⚡ PickMe Flash (Logistics):** Advanced delivery orchestration including "Flash XXL" and heavy-duty logistics support.
*   **🚚 Truck Dispatch System:** Dedicated driver interface for managing 1500kg/10ft truck jobs.
*   **🚲 JumJum Driver Ecosystem:** Dual-mode support for the JumJum sub-brand, including specialized JumJum Wallet.

> [!IMPORTANT]
> **Hardware Binding:** PickMe implements cryptographic binding of driver accounts to physical device IDs to prevent account sharing and fraud.

---
*Proprietary Dissection Record | Lead Prototyper: Nimuthu Ganegoda | Database Manager*

