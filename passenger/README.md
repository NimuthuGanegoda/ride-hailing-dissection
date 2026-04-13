# 🚕 PickMe Passenger: Dissected Features

A comprehensive breakdown of the features and capabilities discovered within the **PickMe Passenger** application (`com.pickme.passenger`).

---

### 📍 Core Services & Logic
*   **Real-Time Tracking & Dispatch:** Uses high-accuracy location services (`ACCESS_FINE_LOCATION`) to track vehicles and provide ETAs. 
*   **Dynamic Pricing & Fare Estimation:** Likely handled by the backend server via API endpoints found in the APK.
*   **Multi-Modal Transport:** Support for cars, tuk-tuks, and even food delivery (indicated by specific API paths).

### 🛠️ Key Capabilities
*   **Integrated Payments:** Uses **CyberSource** for secure credit/debit card transactions and fraud detection. 
*   **Profile & Verification:** Uses the camera and media access for profile management and potentially scanning QR codes. 
*   **Communication:** In-app calling and potentially a chat-based support system.
*   **Intelligent Notifications:** Uses Firebase and GMS services for real-time alerts about trip status and promotions.

### 🧩 Advanced Integrations
*   **ML-Powered Barcode Scanning:** Uses Google's ML Kit for barcode extraction (`oned_feature_extractor_mobile.tflite`).
*   **Referral & Loyalty Programs:** Uses install referrer APIs to track user acquisitions and potentially reward referrals.
*   **Multi-Language Support:** Localized for Sinhala, Tamil, English, and Nepali users.

---
*Analyzed by Gemini CLI for the Database Manager. This document serves as a guide for further architectural dissection.*
