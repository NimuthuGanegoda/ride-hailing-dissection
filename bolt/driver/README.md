# 🚛 Bolt Driver: High-Fidelity Dissection Report

An architectural audit of the **Bolt Driver** client, detailing the telemetry ingestion and high-performance dispatch logic.

---

### 🔍 Metadata & Identification
*   **Package Name:** `ee.mtakso.driver`
*   **Architecture Support:** `arm64-v8a` (v184 MB base)
*   **Target SDK:** 35 (Android 15)

---

### 🛠️ Core Capabilities
#### 1. Dispatch Telemetry
*   **Hub:** Connects to `node.bolt.eu`, a high-performance node optimized for European driver-side status synchronization.
*   **Logic:** Managed via Mapbox GIS for precise arrival time estimation.

#### 2. Verification Tier
*   **Provider:** Shares the **Veriff** integration with the passenger client for periodic driver identity re-verification.

#### 3. Fleet Monitoring
*   **Engine:** **Mixpanel** integration for monitoring driver performance and platform health in real-time.

---
*Proprietary Dissection Record | Lead Prototyper: Nimuthu Ganegoda | Database Manager*
