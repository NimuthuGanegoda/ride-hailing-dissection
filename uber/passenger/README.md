# 📱 Uber Passenger: High-Fidelity Dissection Report

![Platform](https://img.shields.io/badge/Platform-Uber-000000?style=for-the-badge&logo=uber&logoColor=white)
![Tech](https://img.shields.io/badge/Tech-Android%20(APK)-3DDC84?style=for-the-badge&logo=android&logoColor=white)
![Status](https://img.shields.io/badge/Status-Dissected-green?style=for-the-badge)

An exhaustive architectural audit of the **Uber Passenger** application, detailing the global infrastructure, payment systems, and intelligence modules used by the platform.

---

### 🔍 Metadata & Identification
*   **📦 Package Name:** `com.ubercab`
*   **🔢 Version Name:** `4.624.10005` (v10005)
*   **🎯 Target SDK:** 35 (Android 15) | **Min SDK:** 21 (Android 5.0)
*   **🏗️ Platform Support:** Highly optimized for global deployment across a wide range of legacy and modern hardware.

---

### 🛠️ Core Capabilities & Ecosystem
#### 1. 💳 Global Payment Fabric
*   **🛡️ Gateways:** **Braintree** (`api.braintreegateway.com`) and **PayPal** (`api-m.paypal.com`).
*   **🔐 Features:** Implements 3D Secure, Venmo integration, and sophisticated fraud detection via vaulted keys.
*   **💰 Pricing Engine:** Dedicated `PricingApi` for real-time dynamic fare calculation.

#### 2. 📦 Service Coupling (Uber Eats)
*   **🚚 Integration:** Explicit support for food delivery services (`gifting_eats_feature_launcher`).
*   **🧠 Logic:** Tightly integrated modular UI for seamless switching between ride-hailing and logistics.

#### 3. 🧠 Intelligence & Comms
*   **🤖 Waymo Integration (Autonomous):** Direct integration with Waymo for booking autonomous vehicle rides.
*   **🛡️ RideCheck Safety:** Proactive crash and anomaly detection using high-frequency GPS and accelerometer telemetry.
*   **🗺️ GIS Engine:** Connects to `cn-geo1.uber.com` for high-precision geo-fencing and routing.

> [!TIP]
> **Autonomous Ready:** Uber's architecture is already decoupled to support third-party autonomous providers like Waymo as a first-class dispatch tier.

---
*Proprietary Dissection Record | Lead Prototyper: Nimuthu Ganegoda | Database Manager*

