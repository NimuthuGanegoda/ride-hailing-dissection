# 🚛 PickMe Driver: Dissected Features

A comprehensive breakdown of the inner workings and leadership features discovered within the **PickMe Driver** application (`com.pickme.driver.byod`).

---

### 📅 Core Driver Services
*   **Persistent Tracking & Job Dispatch:** Uses background location and foreground services to keep drivers "visible" to the system at all times. 
*   **Driver-Specific Dispatch API:** Connects directly to `driver-api-go.pickme.lk` and `delivery-driver-api.pickme.lk` for ride and delivery requests. 
*   **In-App Support Chat:** Connects to a dedicated `driver-chat-server.pickme.lk` for real-time communication with the control room or passengers.

### 🛠️ Strategic Tools & Controls
*   **System Overlays & Alerts:** Uses `SYSTEM_ALERT_WINDOW` to display incoming jobs over other apps—total dominance over the driver's device. 
*   **Power & Battery Optimization:** Requests exceptions to stay active during long shifts. 
*   **Automated Scheduling & Alarms:** Uses `SCHEDULE_EXACT_ALARM` to ensure drivers aren't late for pre-scheduled pickups.

### 🧩 Backend Integrations & Logic
*   **Self-Registration System:** Includes a portal for drivers to sign up directly via the app (`driver-mobile-self-registration.pickme.lk`). 
*   **ML-Enhanced Scanning:** Similar to the passenger version, uses ML Kit for barcode extraction (`oned_feature_extractor_mobile.tflite`). 
*   **Identity & Fraud Prevention:** Captures device identifiers and phone numbers to ensure driver integrity.

---
*Analyzed by Gemini CLI for the Database Manager. This document serves as a guide for further architectural dissection.*
