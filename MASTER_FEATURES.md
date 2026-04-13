# 📋 Master Feature Inventory: Global Ride-Hailing Industry

A consolidated technical inventory of all features and capabilities identified during the architectural dissection of **PickMe, Uber, Bolt, and Grab**.

---

### 🚗 Core Mobility & Dispatch
*   **On-Demand Ride Booking:** Real-time request-response cycle between passenger and driver nodes.
*   **Multi-Modal Transport:** support for varied vehicle classes (Cars, Tuk-Tuks, Scooters, Luxury, Pool/Share).
*   **Intelligent Fare Estimation:** Dynamic calculation of costs based on distance, estimated time, and route complexity.
*   **Surge & Dynamic Pricing:** Real-time adjustment of pricing algorithms based on local supply and demand density.
*   **GIS & Route Optimization:** High-fidelity mapping integration (Google Maps SDK / Mapbox SDK) for real-time navigation and arrival estimation.

### 🚛 Driver Operational Dominance
*   **Persistent Telemetry Ingestion:** High-frequency ingestion of driver coordinates via background and foreground location services.
*   **Priority Dispatch Engine:** Algorithmic job allocation based on driver proximity, status, and performance metrics.
*   **In-App Earnings Dashboard:** Real-time tracking of daily/weekly earnings, bonuses, and incentives.
*   **System Alert Overlays:** Use of system-level windows to ensure job requests are visible over other applications (Driver Dominance).
*   **Offline Operation Support:** Graceful handling of status synchronization during network degradation.

### 🛡️ Safety, Trust & Integrity
*   **SOS / Emergency Trigger:** Dedicated, high-priority communication paths for immediate assistance during incidents.
*   **Automated Identity Verification:** Use of biometric and document scanning (Veriff / Uber UAM) during onboarding and lifecycle checks.
*   **Trip Sharing (Guardians):** Real-time sharing of trip status and vehicle location with trusted contacts.
*   **Security Protections:** Anti-fraud measures including screen-capture detection and overlay blocking.

### 💳 Financial & Super-App Ecosystem
*   **Integrated Multi-Gateway Payments:** Support for vaulted credit/debit card processing via CyberSource, Braintree, and PayPal.
*   **Loyalty & Reward Engines:** Comprehensive systems for managing promo codes, referral bonuses, and tier-based loyalty points.
*   **In-App Wallets:** Digital currency management for seamless, cashless transactions across all ecosystem services.
*   **Logistical Integration:** Unified support for Food Delivery (Uber Eats / GrabFood) and Package Logistics (PickMe Flash).

### 🧩 Advanced Architectural Features
*   **Modular Feature Delivery:** Use of PlayCore / Feature Patching to load specific capabilities (like carsharing) on-demand.
*   **ML-Powered Vision:** Integration of ML Kit for high-speed barcode and QR code extraction for delivery and profile verification.
*   **Global Localization:** Dynamic support for varied languages (Sinhala, Tamil, Arabic, etc.) and regional GIS data (Karta).
*   **Remote Performance Monitoring:** Real-time exception management and analytics (Mixpanel / MonitorSDK / Firebase).

---
*Synthesized Industry Record | Lead Prototyper: Nimuthu Ganegoda | Database Manager*
