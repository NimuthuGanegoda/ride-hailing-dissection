# Bolt Driver - Technical Analysis

## Overview
Analysis of the Bolt Driver application (ee.mtakso.driver) reveals a focus on high-performance telemetry and modular feature delivery.

## API Endpoints
- `https://node.bolt.eu/`: Primary backend node.
- `https://partners.bolt.eu/`: Partner/Fleet management.
- `https://signup.bolt.eu/`: Driver onboarding portal.
- `https://driver.applog.bolt.eu/`: Specialized logging and telemetry ingestion.
- `https://admin-panel.bolt.eu/`: Administrative oversight and order management.

## Service Keys
- `google_maps_key`: Map rendering and GIS services.
- `google_api_key`: Google Play Services and authentication.

## Feature Flags & Capabilities
- **Modular Feature Delivery**: Uses Kotlin modules for feature delivery (e.g., `playcore_feature_delivery_ktx`).
- **ML-Powered Vision**: Integrated MobileNetV1 for document scanning and biometric verification.
- **Advanced Telemetry**: Specialized endpoints for app logging.

## Core Features
- **Real-time Dispatch**: Optimized job allocation via `node.bolt.eu`.
- **Fleet Management**: Integrated tools for fleet owners and individual drivers.
- **Privacy & Compliance**: Extensive localized privacy and legal resources.
- **Safety**: Face recognition and document validation via on-device ML.
