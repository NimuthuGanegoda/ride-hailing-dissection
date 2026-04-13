# 📱 App-Specific Feature Breakdown

A granular breakdown of the specific features and capabilities embedded within each individual Passenger and Driver application across the global ride-hailing ecosystems.

---

## 🚕 PickMe

### PickMe Passenger (`com.pickme.passenger`)
*   **Multi-Modal Booking:** UI and logic for booking standard rides, Tuk-Tuks, and initiating food/package delivery requests.
*   **Secure Payment Vault:** Integration with CyberSource for tokenized card storage and 3D Secure checkout.
*   **ML Barcode Scanner:** High-speed, on-device QR and barcode scanning for promotions and delivery verification.
*   **Real-Time Tracking Engine:** Live map view with vehicle telemetry and ETA calculations via Google Maps.
*   **Loyalty & Referral Hub:** Referral tracking and promo code application using Install Referrer APIs.

### PickMe Driver (`com.pickme.driver.byod`)
*   **Persistent Dispatch Overlay:** System-alert windows that force job requests to appear over any other app the driver is using.
*   **Self-Registration Portal:** In-app onboarding system for new driver verification and document submission.
*   **In-App Support Chat:** Real-time, dedicated WebSocket/MQTT communication with the central dispatch and support teams.
*   **Strict Power Management:** Bypasses Android battery optimization to ensure the app never sleeps during a shift.
*   **Hardware Binding:** Extensive device ID and phone state reading to bind driver accounts to specific physical phones (Anti-fraud).

---

## ⬛ Uber

### Uber Passenger (`com.ubercab`)
*   **Global Payment Fabric:** Multi-gateway support including Braintree, PayPal, and Venmo, with localized currency handling.
*   **Uber Eats Integration:** Modular UI elements (`gifting_eats_feature_launcher`) allowing seamless transition to food delivery.
*   **Dynamic Pricing Engine:** Real-time fare recalculation based on demand density and geo-fencing (`PricingApi`).
*   **High-Fidelity Media:** ID3 tag extraction and advanced streaming for in-app media or ad experiences.
*   **S2S Analytics:** Server-to-server attribution tracking via Singular.net.

### Uber Driver (`com.ubercab.driver`)
*   **Industrial Telemetry Stream:** High-frequency, continuous background location tracking for precise dispatching.
*   **Modular Verification (BarcodeScanner):** Uses a separate, dynamically loaded APK specifically for high-speed logistical scanning.
*   **Dashboard Projection:** Android Auto templates (`androidx.car.app`) allowing the app to project directly onto the vehicle's head unit.
*   **Screen Capture Detection:** Security measures to prevent unauthorized recording of driver accounts or passenger details.
*   **Remote Feature Flagging:** `DiskFeatureFlag` system for remote A/B testing and on-the-fly capability toggling.

---

## ⚡ Bolt

### Bolt Passenger (`ee.mtakso.client`)
*   **Custom Vector Mapping:** Deep Mapbox SDK integration for customized, European-styled navigation and POI rendering.
*   **Biometric Onboarding:** Deep link integration with Veriff for automated identity and document verification.
*   **Modular Services:** PlayCore Feature Delivery to load carsharing, scooter, or food modules only when requested by the user.
*   **Behavioral Tracking:** Extensive Mixpanel integration for mapping user journeys and optimizing conversion funnels.

### Bolt Driver (`ee.mtakso.driver`)
*   **High-Performance Dispatch:** Optimized European network connections (`node.bolt.eu`) for low-latency job acceptance.
*   **Identity Re-verification:** Periodic biometric checks (via Veriff) to ensure the registered driver is the one operating the vehicle.
*   **Fleet Health Monitoring:** Real-time analytics streaming to monitor app performance and driver interaction states.

---

## 🟢 Grab

### Grab Passenger (`com.grabtaxi.passenger`)
*   **Hyper-Local POI Engine:** Integration with Karta for highly detailed, community-edited mapping specific to Southeast Asia.
*   **Financial Super-App Gateway:** Unified financial tier managing ride payments, GrabFood, and digital wallet balances.
*   **Dynamic UI Patching:** `feature_patch` logic allowing Grab to update the UI and local features without requiring a Play Store update.
*   **Diagnostic Integrity:** MonitorSDK integration to ensure the app functions reliably across varied network conditions.

### Grab Driver (`com.grabtaxi.driver2`)
*   **Logistical Orchestration:** Complex state management for handling concurrent ride, food, and package delivery jobs.
*   **Field POI Uploads:** Capability for drivers to submit map corrections and new points of interest directly from the field.
*   **Regional Onboarding:** Dedicated localized flows for partner registration across different Southeast Asian countries.
*   **Modular Business Logic:** Remote patching system for updating dispatch algorithms and UI components on the fly.

---
*App-Specific Feature Audit | Lead Prototyper: Nimuthu Ganegoda | Database Manager*