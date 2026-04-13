# 🚛 PickMe Driver: High-Fidelity Dissection Report

A rigorous architectural audit of the **PickMe Driver (BYOD)** application, detailing the telemetry, dispatch, and system-level controls used by the platform.

---

### 🔍 Metadata & Identification
*   **Package Name:** `com.pickme.driver.byod`
*   **Version Name:** `37.3.2L` (v739)
*   **Target SDK:** 35 (Android 15) | **Min SDK:** 26 (Android 8.0)
*   **Architecture Support:** `arm64-v8a` (Configured via split APKs)

---

### 🛠️ Core Permission Profile (System Dominance)
The driver client is designed for total persistence and device control to ensure 100% dispatch reliability:
*   **Persistent Tracking:** `ACCESS_BACKGROUND_LOCATION`, `ACCESS_FINE_LOCATION`, `FOREGROUND_SERVICE_LOCATION`.
*   **System Overlays:** `SYSTEM_ALERT_WINDOW` (Allows dispatch alerts to appear over any other active application).
*   **Persistence:** `RECEIVE_BOOT_COMPLETED`, `WAKE_LOCK`, `DISABLE_KEYGUARD`, `REQUEST_IGNORE_BATTERY_OPTIMIZATIONS`.
*   **Scheduling:** `SCHEDULE_EXACT_ALARM` (Ensures critical job alerts are never delayed by OS throttling).
*   **Media & Comms:** `RECORD_AUDIO`, `MODIFY_AUDIO_SETTINGS`, `CAMERA`, `CALL_PHONE`, `READ_CONTACTS`.
*   **Connectivity:** `BLUETOOTH`, `BLUETOOTH_CONNECT`, `ACCESS_WIFI_STATE`, `INTERNET`.

---

### 📍 Architectural Modules
#### 1. Real-Time Dispatch Engine
*   **Protocol:** Utilizes high-frequency telemetry ingestion to sync driver status with the central hub.
*   **Logic:** Managed via `driver-api-go.pickme.lk` for ride-hailing and `delivery-driver-api.pickme.lk` for logistical orchestration.

#### 2. In-App Communication Hub
*   **Chat Server:** Connects to `driver-chat-server.pickme.lk`.
*   **Technology:** Implements real-time messaging for passenger-driver coordination, likely utilizing WebSockets or specialized MQTT-based protocols.

#### 3. Verification & Lifecycle
*   **Self-Registration:** Contains a complete portal for driver on-boarding (`driver-mobile-self-registration.pickme.lk`).
*   **Identity Integrity:** Frequent use of `READ_PHONE_STATE` and `AD_ID` to bind driver accounts to specific physical hardware.
*   **ML Integration:** Shares the same Google ML Kit barcode extraction module as the passenger client for delivery verification.

---

### 🌐 Discovered API Ecosystem
The binary explicitly references these dedicated driver-side services:
*   `https://driver.pickme.lk` - Driver Management Portal
*   `https://driver-api-go.pickme.lk` - High-Performance Dispatch Hub
*   `https://delivery-driver-api.pickme.lk/v0.2/` - Logistics & Delivery API
*   `https://driver-chat-server.pickme.lk` - Secure Comms Server
*   `https://driver-mobile-self-registration.pickme.lk` - Onboarding Gateway

---
*Proprietary Dissection Record | Lead Prototyper: Nimuthu Ganegoda | Database Manager*
