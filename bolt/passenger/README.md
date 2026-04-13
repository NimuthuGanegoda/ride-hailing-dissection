# 📱 Bolt Passenger: High-Fidelity Dissection Report

A technical audit of the **Bolt Passenger** application, focusing on European-market GIS implementations and biometric identity verification.

---

### 🔍 Metadata & Identification
*   **Package Name:** `ee.mtakso.client`
*   **Architecture Support:** `armeabi-v7a` (v118 MB base)
*   **Target SDK:** 35 (Android 15)

---

### 🛠️ Core Capabilities
#### 1. Mapbox GIS Integration
*   **Engine:** Uses **Mapbox SDK** for high-fidelity vector tile rendering and custom navigation styles.
*   **Endpoints:** Connects to `user.live.boltsvc.net` for real-time ride dispatching.

#### 2. Identity Verification (Veriff)
*   **System:** Deeply integrated with **Veriff** (`alchemy.veriff.com`) for automated KYC and document scanning during user onboarding.

#### 3. Behavioral Analytics
*   **Platform:** **Mixpanel** (`api.mixpanel.com`).
*   **Logic:** Tracks detailed user journey metrics to optimize conversion and retention.

---
*Proprietary Dissection Record | Lead Prototyper: Nimuthu Ganegoda | Database Manager*
