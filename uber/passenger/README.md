# 📱 Uber Passenger: High-Fidelity Dissection Report

An exhaustive architectural audit of the **Uber Passenger** application, detailing the global infrastructure, payment systems, and intelligence modules used by the platform.

---

### 🔍 Metadata & Identification
*   **Package Name:** `com.ubercab`
*   **Version Name:** `4.624.10005` (v10005)
*   **Target SDK:** 35 (Android 15) | **Min SDK:** 21 (Android 5.0)
*   **Platform Support:** Highly optimized for global deployment across a wide range of legacy and modern hardware.

---

### 🛠️ Core Capabilities & Ecosystem
#### 1. Global Payment Fabric
*   **Gateways:** **Braintree** (`api.braintreegateway.com`) and **PayPal** (`api-m.paypal.com`).
*   **Features:** Implements 3D Secure, Venmo integration (`venmo.com/go/checkout`), and sophisticated fraud detection via vaulted keys.
*   **Pricing Engine:** Dedicated `PricingApi` for real-time dynamic fare calculation based on supply/demand.

#### 2. Service Coupling (Uber Eats)
*   **Integration:** Explicit support for food delivery services (`gifting_eats_feature_launcher`).
*   **Logic:** Tightly integrated modular UI for seamless switching between ride-hailing and logistics.

#### 3. Intelligence & Comms
*   **GIS Engine:** Connects to `cn-geo1.uber.com` for high-precision geo-fencing and routing.
*   **Analytics:** Extensive use of `singular.net` for S2S (Server-to-Server) attribution and user behavioral tracking.
*   **Media Support:** Includes ID3 tag extraction and high-quality streaming support (`aomedia.org`).

---

### 🌐 Discovered API Ecosystem
The binary explicitly references these global service points:
*   `https://auth.uber.com/v2` - Central Identity & Auth Gateway
*   `https://m.uber.com` - Mobile Web Bridge
*   `https://s2s.singular.net/api/` - Attribution & Marketing Analytics
*   `https://cn-geo1.uber.com/` - Static Content & Geo-data CDN

---
*Proprietary Dissection Record | Lead Prototyper: Nimuthu Ganegoda | Database Manager*
