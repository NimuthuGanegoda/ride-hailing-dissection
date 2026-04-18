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

### 🚀 Unique Platform Features
*   **PickMe Flash (Logistics):** Advanced delivery orchestration including "Flash XXL" and heavy-duty logistics support.
*   **Truck Dispatch System:** Dedicated driver interface for managing 1500kg/10ft truck jobs with specialized routing requirements.
*   **JumJum Driver Ecosystem:** Dual-mode support for the JumJum sub-brand, including specialized JumJum Wallet and anti-fraud hardware binding.
*   **Persistent Dispatch Overlay:** System-level alert windows (`SYSTEM_ALERT_WINDOW`) that force job requests to appear over any other app.
*   **Hardware Binding:** Cryptographic binding of driver accounts to physical device IDs (`READ_PRIVILEGED_PHONE_STATE`) to prevent account sharing/fraud.

---

### 🛠️ Specific App Features
*   **Persistent Dispatch Overlay:** System-alert windows that force job requests to appear over any other app the driver is using.
*   **Self-Registration Portal:** In-app onboarding system for new driver verification and document submission.
*   **In-App Support Chat:** Real-time, dedicated WebSocket/MQTT communication with the central dispatch and support teams.
*   **Strict Power Management:** Bypasses Android battery optimization to ensure the app never sleeps during a shift.
*   **Hardware Binding:** Extensive device ID and phone state reading to bind driver accounts to specific physical phones (Anti-fraud).

### 🌐 Discovered API Ecosystem
The binary explicitly references these dedicated driver-side services:
*   `https://driver.pickme.lk` - Driver Management Portal
*   `https://driver-api-go.pickme.lk` - High-Performance Dispatch Hub
*   `https://delivery-driver-api.pickme.lk/v0.2/` - Logistics & Delivery API
*   `https://driver-chat-server.pickme.lk` - Secure Comms Server
*   `https://driver-mobile-self-registration.pickme.lk` - Onboarding Gateway

---
*Proprietary Dissection Record | Lead Prototyper: Nimuthu Ganegoda | Database Manager*
