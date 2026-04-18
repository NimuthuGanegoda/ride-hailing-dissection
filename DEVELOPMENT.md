# 🛠️ Development & Contribution Guide

Welcome to the **Ride-Hailing Dissection** repository. This project follows a "one-to-one" feature dissection model, where binary evidence is mapped to specific industry capabilities.

## 🏗️ Repository Architecture

The repository is structured by platform and application type, with granular feature reports located in the `features/` subdirectories:

```text
ride-hailing-dissection/
├── bolt/
│   ├── driver/
│   │   └── features/        <-- Granular Driver Feature Reports
│   └── passenger/
│       └── features/        <-- Granular Passenger Feature Reports
├── grab/
├── uber/
└── pickme/
```

## 📝 Dissection Standards

Each feature report (`.md` file) must adhere to the following structure:

1.  **🔍 Binary Evidence:** List specific API endpoints, package names, class references, or string constants found during the dissection.
2.  **⚙️ Technical Logic Summary:** Provide a high-level technical summary of how the feature functions based on the evidence.
3.  **🔗 Reference:** Link the report back to the corresponding entry in the `MASTER_FEATURES.md`.

## 🎨 Visual Assets

Visual representations (SVGs) should be placed in the platform root or relevant application directory and referenced within the Markdown reports using relative paths.

## 🚀 Contribution Workflow

1.  **Identify Feature:** Locate a feature in the binary or network traffic.
2.  **Verify Evidence:** Confirm the strings or endpoints exist across multiple app versions if possible.
3.  **Create Report:** Add a new Markdown file in the appropriate `features/` directory.
4.  **Update Index:** Add the link to the new report in the `MASTER_FEATURES.md` central index.

---
*Lead Developer: Nimuthu Ganegoda | Architectural Prototyper*
