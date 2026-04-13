# 📱 PickMe Passenger: High-Fidelity Dissection Report

A comprehensive technical breakdown of the **PickMe Passenger** application architecture, capabilities, and external integrations.

---

### 🔍 Metadata & Identification
*   **Package Name:** `com.pickme.passenger`
*   **Version Name:** `9.40041-LkPrd` (v863)
*   **Target SDK:** 35 (Android 15) | **Min SDK:** 26 (Android 8.0)
*   **Architecture Support:** `armeabi-v7a` (Configured via split APKs)

---

### 🛠️ Core Permission Profile (Full Audit)
The application requests extensive system access to maintain its real-time dispatch engine:
*   **Location:** `ACCESS_FINE_LOCATION`, `ACCESS_COARSE_LOCATION` (High-precision tracking).
*   **Services:** `FOREGROUND_SERVICE`, `FOREGROUND_SERVICE_MEDIA_PLAYBACK` (Background persistence).
*   **Storage:** `READ_MEDIA_IMAGES`, `READ_EXTERNAL_STORAGE`, `WRITE_EXTERNAL_STORAGE` (Legacy support).
*   **Identity:** `READ_CONTACTS`, `READ_PHONE_STATE`, `READ_PHONE_NUMBERS`.
*   **Connectivity:** `INTERNET`, `ACCESS_NETWORK_STATE`, `ACCESS_WIFI_STATE`, `BLUETOOTH`, `BLUETOOTH_CONNECT`.
*   **System Integrity:** `RECEIVE_BOOT_COMPLETED`, `WAKE_LOCK`, `VIBRATE`, `USE_FULL_SCREEN_INTENT`.

---

### 📍 Architectural Modules
#### 1. Dispatch & GIS Engine
*   **Integration:** Google Maps SDK for Android.
*   **Logic:** Implements complex geo-fencing and route optimization via the `com.samsung.android.mapsagent` and standard GMS GIS providers.
*   **Endpoints:** Bounded to `api.pickme.lk` for real-time fleet visibility.

#### 2. Secure Payment & Fraud Tier
*   **Gateway:** **CyberSource** (`api.cybersource.com`).
*   **Security:** Implements 3D Secure and tokenized payment processing for credit/debit cards.
*   **Loyalty:** Uses `com.android.vending.CHECK_LICENSE` and install referrer clients to track user acquisition and referral rewards.

#### 3. Intelligence & Comms
*   **Messaging:** Integrates Firebase Cloud Messaging (FCM) for push notifications and trip status updates.
*   **Feature Extraction:** Utilizes Google ML Kit (`oned_feature_extractor_mobile.tflite`) for high-speed barcode/QR scanning.
*   **Localisation:** Comprehensive support for Sinhala (`si`), Tamil (`ta`), English (`en`), and Nepali (`ne`).

---

### 🌐 Discovered API Ecosystem
The binary contains references to the following core service points:
*   `https://api.pickme.lk` - Primary Passenger Gateway
*   `https://impression.pickme.lk` - Analytics & User Behavior Tracking
*   `https://monitorsdk.pickme.lk` - Remote Debugging & Exception Management

---
*Proprietary Dissection Record | Lead Prototyper: Nimuthu Ganegoda | Database Manager*
