# 📋 Master Feature Inventory: Global Ride-Hailing Industry

A consolidated technical inventory of all features and capabilities identified during the architectural dissection of **PickMe, Uber, Bolt, and Grab**.

---

### 🚗 Core Mobility & Dispatch
*   **On-Demand Ride Booking:** Real-time request-response cycle between passenger and driver nodes.
    *   [Bolt Passenger Dispatch](bolt/passenger/features/dispatch.md) | [Bolt Driver Dispatch](bolt/driver/features/dispatch.md)
    *   [Grab Passenger Dispatch](grab/passenger/features/dispatch.md) | [Grab Driver Logistics](grab/driver/features/logistics.md)
    *   [Uber Passenger Mobility](uber/passenger/features/mobility.md) | [Uber Driver Dispatch](uber/driver/features/dispatch.md)
    *   [PickMe Passenger Dispatch](pickme/passenger/features/dispatch.md) | [PickMe Driver Dispatch](pickme/driver/features/dispatch.md)
*   **Autonomous Fleet Integration:** Seamless integration of self-driving vehicles (e.g., Waymo) into the on-demand dispatch pool.
    *   [Uber Autonomous Features](uber/passenger/features/mobility.md)
*   **Multi-Modal Transport:** Support for varied vehicle classes and budget-oriented sub-brands (JumJum).
*   **GIS & Route Optimization:** High-fidelity mapping integration for real-time navigation and arrival estimation.
    *   [Bolt Mapping](bolt/passenger/features/mapping.md)
    *   [Grab Mapping](grab/passenger/features/mapping.md) | [Grab Driver Mapping](grab/driver/features/mapping.md)
    *   [Uber Mapping](uber/passenger/features/mapping.md)
    *   [PickMe Mapping](pickme/passenger/features/mapping.md)
*   **Proprietary GIS (GrabMaps):** Custom mapping engine optimized for regional road networks.
    *   [GrabMaps Analysis](grab/passenger/features/mapping.md)

### 🚛 Driver Operational Dominance
*   **Persistent Telemetry Ingestion:** High-frequency ingestion of driver coordinates via background and foreground location services.
    *   [Bolt Driver Telemetry](bolt/driver/features/telemetry.md)
    *   [Grab Driver Telemetry](grab/driver/features/telemetry.md)
    *   [Uber Driver Telemetry](uber/driver/features/telemetry.md)
    *   [PickMe Driver Telemetry](pickme/driver/features/telemetry.md)
*   **System Alert Overlays:** Use of system-level windows to ensure job requests are visible over other applications.
    *   [Uber Driver Overlays](uber/driver/features/dispatch.md)
    *   [PickMe Driver Overlays](pickme/driver/features/dispatch.md)

### 🛡️ Safety, Trust & Integrity
*   **Automated Identity Verification:** Use of biometric and document scanning during onboarding and lifecycle checks.
    *   [Bolt Identity](bolt/passenger/features/identity.md) | [Bolt Driver Identity](bolt/driver/features/identity.md)
    *   [Grab Identity](grab/passenger/features/safety.md) | [Grab Driver Identity](grab/driver/features/safety.md)
    *   [PickMe Driver Identity](pickme/driver/features/identity.md)
*   **Audio Transcription (Safety):** Encrypted trip audio recording for dispute resolution and enhanced safety monitoring.
    *   [Grab Safety](grab/passenger/features/safety.md) | [Grab Driver Safety](grab/driver/features/safety.md)

### 💳 Financial & Super-App Ecosystem
*   **Integrated Multi-Gateway Payments:** Support for vaulted credit/debit card processing.
    *   [Uber Payments](uber/passenger/features/payments.md)
    *   [PickMe Payments](pickme/passenger/features/payments.md)
*   **In-App Wallets & Digital Banking:** Digital currency management and integrated banking services (GXS).
    *   [Grab Financials](grab/passenger/features/financials.md) | [Grab Driver Financials](grab/driver/features/financials.md)
    *   [PickMe Passenger Financials](pickme/passenger/features/payments.md)
*   **Logistical Integration:** Unified support for Food Delivery and Package Logistics.
    *   [Grab Logistics](grab/passenger/features/logistics.md) | [Grab Driver Logistics](grab/driver/features/logistics.md)
    *   [Uber Logistics](uber/passenger/features/logistics.md)
    *   [PickMe Logistics](pickme/passenger/features/logistics.md) | [PickMe Driver Logistics](pickme/driver/features/logistics.md)

### 🧩 Advanced Architectural Features
*   **Modular Feature Delivery:** Use of PlayCore / Feature Patching to load specific capabilities on-demand.
    *   [Bolt Architecture](bolt/passenger/features/architecture.md) | [Bolt Driver Architecture](bolt/driver/features/architecture.md)
    *   [Grab Super-App Architecture](grab/passenger/features/architecture.md)
    *   [Uber Feature Flags](uber/driver/features/architecture.md)
*   **ML-Powered Vision:** Integration of ML Kit for high-speed barcode and QR code extraction.
    *   [PickMe ML Vision](pickme/passenger/features/architecture.md)

---
*Synthesized Industry Record | Lead Developer: Nimuthu Ganegoda | Architectural Prototyper*
