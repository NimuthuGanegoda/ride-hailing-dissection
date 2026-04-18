# 🚛 Grab Driver: High-Fidelity Dissection Report

![Platform](https://img.shields.io/badge/Platform-Grab-00B14F?style=for-the-badge&logo=grab&logoColor=white)
![Tech](https://img.shields.io/badge/Tech-Android%20(APK)-3DDC84?style=for-the-badge&logo=android&logoColor=white)
![Status](https://img.shields.io/badge/Status-Dissected-green?style=for-the-badge)

## 🏛️ Overview
Analysis of the **Grab Driver** application (`com.grabtaxi.driver2`) reveals a complex logistical orchestration platform. It is designed to handle multiple job types (Ride, Food, Mart, Express) concurrently while maintaining high-fidelity telemetry and safety standards.

---

## 🌐 API Endpoints
*   `https://api.grab.com`: Main gateway for job dispatch and status updates.
*   `https://driver-ai.grab.com`: AI-driven safety and fatigue monitoring.
*   `https://map-matching.grab.com`: Real-time GPS snapping and route correction.

---

## 🛠️ Key SDKs & Libraries
*   **🗺️ GrabMaps Driver SDK**: Specialized navigation for high-frequency stop-and-go jobs.
*   **🎙️ Audio Recording SDK**: Continuous/Event-based audio capture for driver safety.
*   **👤 Megvii Face++**: Daily driver identity verification (Selfie check).
*   **📊 MonitorSDK**: Advanced telemetry for performance profiling.

---

## 🚀 Core Features & Capabilities
*   **📦 Modular Job Handling**: Dynamic switching between passenger transport and food delivery workflows.
*   **🗺️ Field-Sourced GIS**: Capability for drivers to report map errors or add new POIs (GrabMaps contribution).
*   **🧠 Fatigue Management**: AI-powered analysis of driving patterns to suggest breaks.
*   **💰 GrabFin Integration**: In-app financial services for vehicle loans and insurance.

> [!TIP]
> **Fatigue AI:** Grab uses a dedicated endpoint `driver-ai.grab.com` to analyze telemetry patterns and proactively manage driver fatigue, enhancing ecosystem safety.

---
*Proprietary Dissection Record | Lead Prototyper: Nimuthu Ganegoda | Database Manager*

