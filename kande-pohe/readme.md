# Kande Pohe Platform

## 📌 Executive Summary
This directory contains the comprehensive manual testing artifacts, functional bug audit, and user workflow evaluations for the **Kande Pohe Web Application**.

The audit covers end-to-end user journeys including onboarding, authentication security, dynamic locale selection, profile data persistence, navigation mechanics, and subscription transaction handling.

---

## 🧪 Modules Audited

1. **Login & Registration Module**: Password policy validation, input constraints, default input state, and localization toggles.
2. **Profile & Lifestyle Setup**: Data mapping types, automated value overrides, age calculation triggers, and edit-save persistence.
3. **Media Upload & Navigation**: Mobile asset uploads, scroll-state restoration, card click targets, and post-authentication routing.
4. **Subscription & Payment Gateway**: Order cancellation state handling and modal loader lifecycle.

---

## 🐛 Defect Master Log

### 1. Authentication, Localization & Onboarding

| Bug ID | Module | Defect Summary & Observed Behavior | Severity |
| :--- | :--- | :--- | :--- |
| **KP-BUG-01** | Login Page | **Calendar Range Limitation**: Date picker dropdown does not load up to the current year, preventing standard age selection. | Major |
| **KP-BUG-02** | Login Page | **Locale Switcher Lock**: Switching language to Marathi locks the UI state; attempting to roll back to English fails and retains Marathi display. | Major |
| **KP-BUG-03** | Registration | **Missing Step-by-Step Localization**: Language switching controls are missing across registration workflow steps. | Medium |
| **KP-BUG-04** | Registration | **Weak Password Validation**: Accepts short passwords (3–5 characters) without enforcing minimum length rules or special character constraints. | Critical |
| **KP-BUG-05** | Registration | **Persistent Input Autofill**: Name field defaults to "Kiran" and retains this value even after manual edits. | Medium |

---

### 2. User Profile, Data Mapping & Persistence

| Bug ID | Module | Defect Summary & Observed Behavior | Severity |
| :--- | :--- | :--- | :--- |
| **KP-BUG-06** | Profile Setup | **Verification Visual Logic**: Visual checkmark indicators fail to update sequentially upon verifying completion steps. | Minor |
| **KP-BUG-07** | Profile Setup | **Mobile Media Upload Failure**: Photo upload trigger is completely non-functional on mobile web browsers. | Critical |
| **KP-BUG-08** | Basic Info | **Missing Age Calculation**: Age field is not prompted during registration and fails to auto-calculate from the selected birthdate. | Medium |
| **KP-BUG-09** | Basic Info | **Unauthorized Field Autofill**: "Mother Tongue" automatically defaults to Marathi instead of prompting user input during registration. | Medium |
| **KP-BUG-10** | Basic Info | **Sub-Community Override**: Sub-community automatically defaults to "96K Maratha", ignoring different user-selected values entered during registration. | Major |
| **KP-BUG-11** | Lifestyle Section | **Raw Numeric Data Display**: Skin Tone, Body Type, and Diet fields display raw integer database IDs instead of human-readable text labels. | Major |
| **KP-BUG-12** | Profile Editing | **Data Update Persistence Failure**: Saving updated profile details fails to write changes; re-opening displays stale previous data. | Critical |

---

### 3. Navigation, UX & Subscription Gateway

| Bug ID | Module | Defect Summary & Observed Behavior | Severity |
| :--- | :--- | :--- | :--- |
| **KP-BUG-13** | Authentication | **Incorrect Post-Login Routing**: Successful authentication routes users directly to the "Inbox" view instead of the main "Dashboard". | Medium |
| **KP-BUG-14** | Home Page | **Scroll Position Reset**: Navigating back from a profile view resets the Home Page scroll position back to the top of the page. | Minor |
| **KP-BUG-15** | Home Page | **Constrained Card Click Target**: "Perfect Match" profile cards do not open when clicking the card image or container; interaction is strictly constrained to the "View Profile" text button. | Minor |
| **KP-BUG-16** | Subscription | **Infinite Loader on Cancellation**: Canceling a subscription workflow before completing payment leaves the application stuck in an infinite loading state (requires pressing back 4 times to break loop). | Major |

---

## 🔍 Key Quality Insights

- **Data Integrity & Mapping**: Numeric data rendering in lifestyle attributes indicates missing frontend dictionary mappers for ENUM values.
- **Form State Overrides**: Sub-community and mother-tongue fields exhibit unhandled hardcoded default overrides during payload construction.
- **Workflow State Locks**: Unhandled exception states in both the language switcher and subscription cancellation workflows lock the UI event loop.
