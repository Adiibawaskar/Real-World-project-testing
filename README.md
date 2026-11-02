# QA Engineering & Software Testing Portfolio

Welcome to my Software Quality Assurance and Web Auditing repository. This repository showcases real-world Manual Testing, Responsive UI/UX Audits, Functional Bug Logging, and Defect Lifecycle Management across production web platforms.

## 📌 Repository Overview

This portfolio contains comprehensive test execution logs, defect reports, and severity assessments for two web applications:

1. **[Kande Pohe Web Platform](./kande-pohe/README.md)**: Consumer web application testing focusing on user authentication, locale dynamic switching, dynamic UI verification controls, and file upload modules.
2. **[College ERP & Admin Portal](./college-erp/README.md)**: Enterprise web application testing covering Super-Admin operations, multi-module data synchronization, responsive viewports, dynamic dashboards, and transactional notifications.

---

## 🛠️ Testing Methodology & Skill Stack

- **Testing Types**: Manual Functional Testing, UI/UX Auditing, Cross-Device Responsive Testing (Desktop vs Mobile Viewports), Module Navigation Testing.
- **Defect Management**: Comprehensive Defect Logging (Module, Description, Root Cause Analysis, Execution Status, Verification Tracking).
- **Core Focus Areas**:
  - **Form Validation & Constraints**: Input bounds checking (e.g., numeric limits, length boundaries).
  - **Asynchronous & Email Workflows**: Verification of dynamic triggers, reset passswords, and modal pop-ups.
  - **UI/UX Consistency**: Alignment audits, icon/asset inversions, chart color key mismatches, and layout overflows.
  - **Cross-Device Responsiveness**: Breakdown audits across mobile viewports for data tables, sub-module directories, and analytics components.

---

## 📊 Summary of Identified Defect Categories

| Category | Description | Primary Impact Areas |
| :--- | :--- | :--- |
| **Responsive & UI Layout** | Elements overflowing viewport boundaries, misaligned buttons, and clipped table pagination in mobile view | Admin Dashboards, Notice Boards, Custom Notifications |
| **Functional & Logic** | Broken file viewing triggers, missing email dispatches, and infinite loading modals | Password Resets, Assignment Directory, File Uploads |
| **Data & Visual Analytics** | Legend color mismatching, chart key discrepancies, and unlabelled dashboard counters | Central Library Overview, Helpdesk Analytics |
| **UI Symbol Inversions** | Swapped directional iconography for data operations | Import / Export Action Buttons |

---

## 📁 Repository Directory Structure

```text
.
├── README.md                          # Repository Root & Executive Summary
├── kande-pohe/
│   └── README.md                      # Kande Pohe Web Platform Bug Audit
└── college-erp/
    └── README.md                      # College ERP & Admin System Bug Audit
