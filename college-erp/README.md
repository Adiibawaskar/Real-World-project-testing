# Real-World Web Audit: Enterprise College ERP System

## 📌 Executive Summary
This directory houses the comprehensive quality assurance audit for an **Enterprise College ERP System**. The audit spans multiple access tiers (Super-Admin, Faculty, Student, and Library Operations) across mobile and desktop viewports, focusing on responsive structural layouts, data visualizers, and transactional communications.

---

## 🧪 Functional Areas & Sub-Modules Audited

- **Super-Admin & Management**: Institution Types, Ownership/Affiliation UI, Custom Notifications.
- **Faculty & Student Directories**: Password recovery triggers, modal handling, and profile photo updates.
- **Central Library & Catalogue**: Chart color key consistency, mobile pagination layout, ISBN input bounds, and edition year validation.
- **Campus Broadcast & Assignments**: Notice board attachments, event calendar media renders, and reference file previewing.
- **Analytics & Helpdesk**: Chart axis label positioning, ticket table frame limits, and sub-module navigation responsiveness.

---

## 🐛 Defect Master Log

### 1. High-Severity & Functional Logic Defects

| Bug ID | Module | Defect Summary & Root Cause Analysis | Severity |
| :--- | :--- | :--- | :--- |
| **ERP-BUG-01** | Password Recovery (Faculty/Student) | **SMTP Dispatch & Infinite Modal Lock**: Password reset fails to dispatch emails consistently. Modal dialog remains in an infinite loading state and cannot be closed by the user. | Critical |
| **ERP-BUG-02** | Assignments Directory | **Reference Document View Failure**: Action column icon to view/download reference documents fails to load files, outputting broken links upon opening. | High |
| **ERP-BUG-03** | Campus Broadcast | **Event & Notice Image Render Failure**: Event images upload successfully but fail to render inside table views or public broadcast notice boards after publishing. | High |
| **ERP-BUG-04** | Faculty Directory | **Profile Media Sync Defect**: Profile photo update triggers a success toast notification, but media is not updated on the table icon or user profile page. | Medium |
| **ERP-BUG-05** | Book Catalogue | **ISBN Input Validation Absence**: ISBN field accepts unbounded length and non-numeric inputs. Missing standard 13-digit numeric validation[cite: 1.3]. | Medium |
| **ERP-BUG-06** | Book Catalogue | **Year Boundary Constraint**: "Publication Year / Edition" field rejects input values beyond 2099. | Low |

---

### 2. UI/UX, Chart Visualizers & Iconography Defects

| Bug ID | Module | Defect Summary & Visual Discrepancy | Severity |
| :--- | :--- | :--- | :--- |
| **ERP-BUG-07** | Central Library Overview | **Pie Chart Legend Mismatch**: Chart legend maps "Issued Books" to blue color, while the chart slice renders in white. Data counts do not align with library stats. | Medium |
| **ERP-BUG-08** | Book Catalogue | **UI Icon Inversion**: Import and export symbols are swapped globally across all data operation buttons throughout the application. | Medium |
| **ERP-BUG-09** | Campus Broadcast | **Dashboard Card Label Absence**: Main broadcast dashboard displays metric numbers without descriptive card titles. | Low |
| **ERP-BUG-10** | Helpdesk Analytics | **Axis Label Alignment**: Bar graph X-axis labels are misaligned beneath bar structures, rendering ticket names unreadable. | Low |

---

### 3. Cross-Device Responsive & Mobile Viewport Defects

| Bug ID | Module | Viewport Bug Description | Severity |
| :--- | :--- | :--- | :--- |
| **ERP-BUG-11** | Custom Notifications | Add Notification button contains duplicated text (`++Add Notification`) and overflows screen bounds in Mobile View. | Medium |
| **ERP-BUG-12** | Logbook Manager | Logbook Management table and top search bar lack horizontal scrolling and responsive behavior on both desktop and mobile screens. | Medium |
| **ERP-BUG-13** | Master Data & UI | Institution Type, Ownership Data, and Affiliation Data UI buttons misalign under Mobile Viewports. | Low |
| **ERP-BUG-14** | Multi-Module Nav | Mobile view overflow detected in Library Navigation, Assignment Analytics, Clinical Navigation, and Notice Directories. | Low |

---

## 🛠️ Testing Environment Details

- **Target Platforms**: Desktop (Chrome, Edge) & Mobile Viewport Emulation.
- **Reporting Format**: Standardized Defect Tracking Matrix.
