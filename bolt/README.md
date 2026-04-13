# ⚡ Bolt Ecosystem: High-Fidelity Dissection Report

A rigorous architectural audit of the **Bolt** (formerly Taxify) applications, detailing the European-centric infrastructure, identity verification, and modular feature delivery systems.

---

### 🔍 Metadata & Identification
*   **Passenger Client:** `ee.mtakso.client` (v118 MB)
*   **Driver Client:** `ee.mtakso.driver` (v184 MB)
*   **Architecture Support:** `armeabi-v7a` and `arm64-v8a` (via split APKs)

---

### 🛠️ Core Capabilities & Ecosystem
#### 1. Advanced GIS & Mapping
*   **Provider:** **Mapbox SDK** (`apps.mapbox.com`).
*   **Capabilities:** Implements custom Mapbox Standard styles with high-frequency telemetry for real-time routing and ETA calculations.

#### 2. Identity & Trust (Veriff Integration)
*   **System:** **Veriff** (`alchemy.veriff.com`).
*   **Logic:** Uses automated biometric and document verification to ensure driver and passenger integrity, highly integrated into the sign-up and lifecycle flows.

#### 3. Industrial Analytics (Mixpanel)
*   **Engine:** **Mixpanel** (`api.mixpanel.com`).
*   **Telemetry:** Captures exhaustive people-profile properties and event-driven data to optimize fleet allocation and user retention.

#### 4. Modular Feature Delivery
*   **Technology:** Uses Google PlayCore Feature Delivery (`playcore_feature_delivery`).
*   **Features:** Allows the app to remain lean by loading specific modules (like carsharing or scooters) on demand.

---

### 🌐 Discovered API Ecosystem
The binaries explicitly reference these central service points:
*   `https://bolt.eu/` - Corporate & User Web Bridge
*   `https://user.live.boltsvc.net/` - Core Passenger API Service
*   `https://node.bolt.eu/` - High-Performance Driver Dispatch Hub
*   `https://bolt.sng.link/` - Singular Attribution & Deep Linking

---
*Proprietary Dissection Record | Lead Prototyper: Nimuthu Ganegoda | Database Manager*
