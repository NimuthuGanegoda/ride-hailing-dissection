# 💳 Global Payment Fabric: Uber Passenger

### 🔍 Binary Evidence
*   **Gateways:** **Braintree** (`api.braintreegateway.com`), **PayPal** (`api-m.paypal.com`), and **Venmo**.
*   **Pricing Engine:** `PricingApi` for dynamic fare calculation.
*   **Security:** Implements 3D Secure and vaulted payment processing.

### ⚙️ Technical Logic Summary
Uber's payment architecture is a multi-gateway system that handles global and local payment methods seamlessly. The pricing engine calculates fares in real-time based on demand density, supply, and route complexity, using vaulted keys for secure transaction processing.

### 🔗 Reference
*   **MASTER_FEATURES.md:** [Integrated Multi-Gateway Payments], [Surge & Dynamic Pricing]
