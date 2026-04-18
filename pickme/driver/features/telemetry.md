# 🚛 Telemetry & Operational Dominance: PickMe Driver

### 🔍 Binary Evidence
*   **Persistence:** `RECEIVE_BOOT_COMPLETED`, `WAKE_LOCK`, `DISABLE_KEYGUARD`.
*   **Power Optimization:** `REQUEST_IGNORE_BATTERY_OPTIMIZATIONS`, `SCHEDULE_EXACT_ALARM`.
*   **Persistent Location:** `ACCESS_BACKGROUND_LOCATION`, `ACCESS_FINE_LOCATION`, `FOREGROUND_SERVICE_LOCATION`.

### ⚙️ Technical Logic Summary
The driver application ensures 100% dispatch availability through deep system-level persistence. It bypasses OS throttling via exact alarm scheduling and battery optimization requests, maintaining a continuous location stream even when the device is locked or in standby.

### 🔗 Reference
*   **MASTER_FEATURES.md:** [Persistent Telemetry Ingestion], [System Alert Overlays]
