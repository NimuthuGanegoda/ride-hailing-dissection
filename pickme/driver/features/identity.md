# 🛡️ Identity & Security: PickMe Driver

### 🔍 Binary Evidence
*   **Onboarding:** In-app **Self-Registration Portal** (`driver-mobile-self-registration.pickme.lk`).
*   **Anti-Fraud:** **Hardware Binding** via `READ_PRIVILEGED_PHONE_STATE`.
*   **Logic:** Uses `READ_PHONE_STATE` and `AD_ID` to bind accounts to physical hardware.

### ⚙️ Technical Logic Summary
Identity is maintained through deep cryptographic binding between the driver account and physical device hardware. This ensures that accounts cannot be shared across multiple phones, providing a strong anti-fraud layer and ensuring only authorized drivers are active on the platform.

### 🔗 Reference
*   **MASTER_FEATURES.md:** [Automated Identity Verification], [Security Protections]
