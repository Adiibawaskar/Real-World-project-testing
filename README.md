# QA Engineering & Software Testing Portfolio

Welcome to my Software Quality Assurance and Web Auditing repository (**`Real-World-project-testing`**). This repository showcases real-world Manual Testing, Responsive UI/UX Audits, Functional Defect Logging, and Performance Root-Cause Analyses across production web platforms.

## 📌 Repository Overview

This portfolio contains structured defect reports, severity categorizations, and test execution matrices for two web applications:

1. **[Kande Pohe Web Platform](./kande-pohe/README.md)**: Consumer web application testing focusing on user authentication, localization rollbacks, profile data persistence, input validation, navigation scroll restoration, and payment gateway cancellation handlers.
2. **[College ERP & Admin Portal](./college-erp/README.md)**: Enterprise web application testing covering Super-Admin operations, multi-module data synchronization, responsive viewports, dynamic dashboards, N+1 backend latency optimization, and transactional notification flows.

---

## 🛠️ Testing Methodology & Skill Stack

- **Testing Types**: Manual Functional Testing, UI/UX Auditing, Cross-Device Responsive Testing (Desktop vs. Mobile Viewports), Boundary Value Analysis (BVA), Navigation & State Restoration Testing.
- **Defect Management**: Comprehensive Defect Logging (Module, Technical Description, Root Cause Analysis, Severity Assessment).
- **Core Focus Areas**:
  - **Form Validation & Security**: Input length limits, password strength rules, and unhandled default value overrides.
  - **State & Data Persistence**: Data mapping verification (ENUM to string display), profile write-back persistence, and locale rollback handling.
  - **Asynchronous & Gateway Workflows**: Modal loading lockouts, payment cancellation loops, and email dispatch triggers.
  - **UI/UX & Responsiveness**: Mobile viewport overflow checks, icon orientation consistency, chart legend mapping, and touch/click target area audits.

---

## 📊 Summary of Defect Breakdown

| Category | Description | Primary Impact Areas |
| :--- | :--- | :--- |
| **Functional & Logic** | Missing input validation, broken file opening triggers, unauthorized field overrides, and infinite loading modals | Password Selection, Profile Setup, Subscription Gateway, Assignments |
| **Data Mapping & State** | Raw numeric IDs displayed in UI, lost edit updates, lost scroll positions, and locked language toggles | Lifestyle Info, Basic Info, Home Navigation, Localization |
| **Responsive & Layout** | Viewport overflows, misaligned buttons, restricted click target containers, and clipped data tables | Admin Dashboards, Notice Boards, Profile Cards, Custom Notifications |
| **Data & Visual Analytics** | Chart color key mismatches, misaligned axis labels, missing card labels, and swapped icon buttons | Central Library, Campus Broadcast, Import/Export Tools |
| **Backend Performance** | High latency dashboard rendering caused by 11 sequential queries and N+1 query loops | Super-Admin Dashboard Overview |

---

## 📁 Repository Directory Structure

```text
.
├── README.md                          # Repository Root & Portfolio Overview
├── kande-pohe/
│   ├── README.md                      # Kande Pohe Web Platform Bug Audit
│   └── assets/                        # Defect Screenshots & Visual Evidence
└── college-erp/
    ├── README.md                      # College ERP & Admin System Bug Audit
    └── assets/                        # Defect Screenshots & Visual Evidence
