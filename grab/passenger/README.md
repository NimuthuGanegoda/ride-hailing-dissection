# Grab Passenger - Technical Analysis

## Overview
Analysis of the Grab Passenger application (`com.grabtaxi.passenger`) reveals a highly integrated "Super App" architecture. It consolidates transportation, logistics, and financial services into a single platform with heavy emphasis on regional localization and safety.

## API Endpoints
- `https://api.grab.com`: Primary backend API gateway.
- `https://api2.grab.com`: Secondary/Legacy API cluster.
- `https://api.grabpay.com`: Dedicated financial services and wallet endpoint.
- `https://grabmaps.grab.com`: Grab's proprietary mapping and GIS services.
- `https://food.grab.com`: GrabFood delivery orchestration.
- `https://data-api.grab.com`: Telemetry and data ingestion.
- `https://partner-api.grab.com`: Third-party integration gateway.
- `https://api.gxs.com.sg`: GXS Bank (Digital Bank) integration.
- `https://api.sg.gdefence.io`: Anti-fraud and safety signaling.
- `https://api.moca.vn`: Vietnamese payment partner (Moca) integration.

## Key SDKs & Libraries
- **GrabMaps SDK** (`com.grab.mapsdk`): Proprietary GIS engine replacing/supplementing Google Maps.
- **GrabPay SDK** (`com.grab.payments`): Full-stack digital wallet and payment processing.
- **Grab Safety SDK**: Integrated audio recording and safety monitoring.
- **Megvii Face++** (`com.megvii`): Biometric verification and facial recognition.
- **Circle SDK**: Web3 and stablecoin infrastructure components.
- **Karta POI** (`com.grab.karta.poi`): Hyper-local community-sourced mapping data.

## Feature Flags & Capabilities
- **Super App Orchestration**: Modular loading of "Grablets" (mini-apps) for Food, Mart, and Finance.
- **Dynamic UI Patching**: Uses `feature_patch` logic for real-time UI updates without app store releases.
- **Audio Safety Monitoring**: Real-time audio recording capability during trips for dispute resolution.
- **GXS Bank Integration**: Direct linkage with digital banking services in Singapore.

## Core Features
- **GrabMaps**: Custom navigation engine optimized for Southeast Asian road networks (narrow alleys, local shortcuts).
- **GrabFood & Bill Splitting**: Advanced group ordering with the ability to split bills equally or by person.
- **GrabPay & PayLater**: Integrated credit lines (Buy Now Pay Later) and cross-border digital payments.
- **Audio Transcription (Safety)**: Encrypted audio recording feature that can be enabled for added trip security.
- **Multi-Modal Transport**: Support for Cars, Bikes, Tuk-tuks (GrabThrone), and cross-border bus bookings.

---
*Proprietary Dissection Record | Lead Prototyper: Nimuthu Ganegoda | Database Manager*
