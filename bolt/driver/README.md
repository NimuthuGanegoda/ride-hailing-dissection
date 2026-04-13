# 🚛 Bolt Driver: High-Fidelity Dissection Report

An architectural audit of the **Bolt Driver** client, detailing the telemetry ingestion and high-performance dispatch logic.

### 🛠️ Specific App Features
*   **High-Performance Dispatch:** Optimized European network connections (`node.bolt.eu`) for low-latency job acceptance.
*   **Identity Re-verification:** Periodic biometric checks (via Veriff) to ensure the registered driver is the one operating the vehicle.
*   **Fleet Health Monitoring:** Real-time analytics streaming to monitor app performance and driver interaction states.

---

### 🔍 Metadata & Identification
*   **Package Name:** `ee.mtakso.driver`
*   **Architecture Support:** `arm64-v8a` (v184 MB base)
*   **Target SDK:** 35 (Android 15)

### 🛠️ Specific App Features
*   **High-Performance Dispatch:** Optimized European network connections (`node.bolt.eu`) for low-latency job acceptance.
*   **Identity Re-verification:** Periodic biometric checks (via Veriff) to ensure the registered driver is the one operating the vehicle.
*   **Fleet Health Monitoring:** Real-time analytics streaming to monitor app performance and driver interaction states.

---

### 🛠️ Core Capabilities
#### 1. Dispatch Telemetry
*   **Hub:** Connects to `node.bolt.eu`, a high-performance node optimized for European driver-side status synchronization.
*   **Logic:** Managed via Mapbox GIS for precise arrival time estimation.

#### 2. Verification Tier
*   **Provider:** Shares the **Veriff** integration with the passenger client for periodic driver identity re-verification.

#### 3. Fleet Monitoring
*   **Engine:** **Mixpanel** integration for monitoring driver performance and platform health in real-time.

### 🛠️ Specific App Features
*   **High-Performance Dispatch:** Optimized European network connections (`node.bolt.eu`) for low-latency job acceptance.
*   **Identity Re-verification:** Periodic biometric checks (via Veriff) to ensure the registered driver is the one operating the vehicle.
*   **Fleet Health Monitoring:** Real-time analytics streaming to monitor app performance and driver interaction states.

---
*Proprietary Dissection Record | Lead Prototyper: Nimuthu Ganegoda | Database Manager*
