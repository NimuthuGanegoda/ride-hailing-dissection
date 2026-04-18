# 📱 Grab Passenger: High-Fidelity Dissection Report

![Platform](https://img.shields.io/badge/Platform-Grab-00B14F?style=for-the-badge&logo=grab&logoColor=white)
![Tech](https://img.shields.io/badge/Tech-Android%20(APK)-3DDC84?style=for-the-badge&logo=android&logoColor=white)
![Status](https://img.shields.io/badge/Status-Dissected-green?style=for-the-badge)

## 🏛️ Overview
Analysis of the **Grab Passenger** application (`com.grabtaxi.passenger`) reveals a highly integrated "Super App" architecture. It consolidates transportation, logistics, and financial services into a single platform with heavy emphasis on regional localization and safety.

---

## 🌐 API Endpoints
*   `https://api.grab.com`: Primary backend API gateway.
*   `https://grabmaps.grab.com`: Grab's proprietary mapping and GIS services.
*   `https://api.gxs.com.sg`: GXS Bank (Digital Bank) integration.
*   `https://api.sg.gdefence.io`: Anti-fraud and safety signaling.

---

## 🛠️ Key SDKs & Libraries
*   **🗺️ GrabMaps SDK** (`com.grab.mapsdk`): Proprietary GIS engine replacing/supplementing Google Maps.
*   **💳 GrabPay SDK** (`com.grab.payments`): Full-stack digital wallet and payment processing.
*   **🛡️ Grab Safety SDK**: Integrated audio recording and safety monitoring.
*   **👤 Megvii Face++** (`com.megvii`): Biometric verification and facial recognition.

---

## 🚀 Core Features & Capabilities
*   **📦 Super App Orchestration**: Modular loading of "Grablets" (mini-apps) for Food, Mart, and Finance.
*   **🏗️ Dynamic UI Patching**: Uses `feature_patch` logic for real-time UI updates without app store releases.
*   **🎙️ Audio Safety Monitoring**: Real-time audio recording capability during trips for dispute resolution.
*   **💰 GXS Bank Integration**: Direct linkage with digital banking services in Singapore.

> [!IMPORTANT]
> **GrabMaps Analysis:** Grab has significantly decoupled from GMS/Mapbox by implementing its own proprietary GIS stack (GrabMaps) optimized for Southeast Asian road networks.

---
*Proprietary Dissection Record | Lead Prototyper: Nimuthu Ganegoda | Database Manager*

