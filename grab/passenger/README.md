# 📱 Grab Passenger: High-Fidelity Dissection Report

A technical breakdown of the **Grab "Super App"** architecture, focusing on Southeast Asian regional services and financial tier.

---

### 🔍 Metadata & Identification
*   **Package Name:** `com.grabtaxi.passenger`
*   **Architecture Support:** `arm64-v8a` (v287 MB base)
*   **Target SDK:** 35 (Android 15)

---

### 🛠️ Core Capabilities
#### 1. Regional GIS (Karta)
*   **Engine:** Integrated with **Karta POI API** (`com.grab.karta.poi`) for hyper-local mapping data in Southeast Asian markets.

#### 2. Financial Super-App Hub
*   **Central API:** `api.grab.com`.
*   **Features:** Manages diverse services including Transport, Food, and Delivery through a unified financial gateway.

#### 3. Localization & Integrity
*   **Monitoring:** Uses **MonitorSDK** for remote debugging and ensuring uptime across inconsistent regional networks.

---
*Proprietary Dissection Record | Lead Prototyper: Nimuthu Ganegoda | Database Manager*
