# Grab Driver - Technical Analysis

## Overview
Analysis of the Grab Driver application (`com.grabtaxi.driver2`) reveals a complex logistical orchestration platform. It is designed to handle multiple job types (Ride, Food, Mart, Express) concurrently while maintaining high-fidelity telemetry and safety standards.

## API Endpoints
- `https://api.grab.com`: Main gateway for job dispatch and status updates.
- `https://driver-ai.grab.com`: AI-driven safety and fatigue monitoring.
- `https://map-matching.grab.com`: Real-time GPS snapping and route correction.
- `https://geo-tools.grabtaxi.com`: Tools for driver-contributed POI and map updates.
- `https://iot-app-ui.grab.com`: Interface for telematics and external IoT integrations.
- `https://paysi.grabtaxi.com`: Driver earnings and payout orchestration.
- `https://cdn-settings.grab.com`: Dynamic configuration and regional feature flags.

## Key SDKs & Libraries
- **GrabMaps Driver SDK**: Specialized navigation for high-frequency stop-and-go jobs.
- **Audio Recording SDK**: Continuous/Event-based audio capture for driver safety.
- **Megvii Face++**: Daily driver identity verification (Selfie check).
- **MonitorSDK**: Advanced telemetry for performance profiling across low-end devices.
- **Bugsee**: Visual bug reporting and crash analytics.

## Feature Flags & Capabilities
- **Modular Job Handling**: Dynamic switching between passenger transport and food delivery workflows.
- **Field-Sourced GIS**: Capability for drivers to report map errors or add new POIs (GrabMaps contribution).
- **Fatigue Management**: AI-powered analysis of driving patterns to suggest breaks.
- **GrabFin Integration**: In-app financial services for vehicle loans and insurance.

## Core Features
- **GrabMaps Navigation**: In-app navigation optimized for heavy vehicles and motorcycle lanes.
- **Safety Audio Recording**: Encrypted recording of trip audio to protect drivers from false accusations.
- **Instant Payouts**: Real-time transfer of earnings to the GrabPay wallet or linked bank accounts.
- **Job Auto-Accept**: Intelligent queuing system to minimize idle time between jobs.
- **Heatmaps**: Real-time demand visualization based on historical and live data.

---
*Proprietary Dissection Record | Lead Prototyper: Nimuthu Ganegoda | Database Manager*
