# 🚛 Grab Driver: High-Fidelity Dissection Report

An architectural audit of the **Grab Driver** platform, detailing the logistical orchestration and modular patching systems.

### 🛠️ Specific App Features
*   **Logistical Orchestration:** Complex state management for handling concurrent ride, food, and package delivery jobs.
*   **Field POI Uploads:** Capability for drivers to submit map corrections and new points of interest directly from the field.
*   **Regional Onboarding:** Dedicated localized flows for partner registration across different Southeast Asian countries.
*   **Modular Business Logic:** Remote patching system for updating dispatch algorithms and UI components on the fly.

---

### 🔍 Metadata & Identification
*   **Package Name:** `com.grabtaxi.driver2`
*   **Architecture Support:** `arm64-v8a` (v291 MB base)
*   **Target SDK:** 35 (Android 15)

### 🛠️ Specific App Features
*   **Logistical Orchestration:** Complex state management for handling concurrent ride, food, and package delivery jobs.
*   **Field POI Uploads:** Capability for drivers to submit map corrections and new points of interest directly from the field.
*   **Regional Onboarding:** Dedicated localized flows for partner registration across different Southeast Asian countries.
*   **Modular Business Logic:** Remote patching system for updating dispatch algorithms and UI components on the fly.

---

### 🛠️ Core Capabilities
#### 1. Logistical Telemetry
*   **Protocol:** High-frequency ingestion of driver status and location data via `api.grab.com`.
*   **Mapping:** Deep Karta integration for driver-side navigation and POI updates.

#### 2. Dynamic Patching System
*   **Technology:** Uses `feature_patch` logic to deploy rapid UI and business logic updates to partners without full app updates.

#### 3. Operational Monitoring
*   **Hub:** Connects to `cdn-settings.grab.com` for regional configuration and partner-specific onboarding flows (`register.grab.com`).

### 🛠️ Specific App Features
*   **Logistical Orchestration:** Complex state management for handling concurrent ride, food, and package delivery jobs.
*   **Field POI Uploads:** Capability for drivers to submit map corrections and new points of interest directly from the field.
*   **Regional Onboarding:** Dedicated localized flows for partner registration across different Southeast Asian countries.
*   **Modular Business Logic:** Remote patching system for updating dispatch algorithms and UI components on the fly.

---
*Proprietary Dissection Record | Lead Prototyper: Nimuthu Ganegoda | Database Manager*
