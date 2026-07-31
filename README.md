# 🚇 Smart Metro Ticket Booking System

A **ServiceNow-based digital ticket booking solution** for metro rail commuters — enabling passengers to search routes, view fares, pay digitally, and receive a QR-code ticket in minutes, without visiting a counter.

---

## 📌 Problem Statement

Commuters travelling by metro rail face long queues, manual fare calculation errors, limited counter timings, and dependency on physical tokens/tickets — leading to delays, overcrowding, and an inconvenient travel experience, especially during peak hours and for first-time or differently-abled passengers.

## 💡 Proposed Solution

The system digitizes the entire booking-to-travel journey on the **Now Platform**:

1. Passenger selects source & destination from a searchable Service Catalog form.
2. Fare is calculated instantly (with auto-applied Student/Senior Citizen discounts).
3. Passenger pays via UPI, card, or wallet.
4. A unique, single-use QR ticket is generated and delivered via app notification, email, and WhatsApp/SMS.
5. The QR code is validated at the station gate in real time.

Every step is logged for audit, reporting, and exception handling.

---

## ✨ Key Features

- 🎫 Searchable Service Catalog booking form with station validation
- 💰 Real-time, itemized fare calculation with automatic discounts
- 💳 Digital payments (UPI / Card / Wallet) with retry-on-failure handling
- 📱 Instant, single-use QR ticket generation
- 🔔 Multi-channel ticket delivery (in-app, email, WhatsApp/SMS)
- 📜 Booking history & ticket re-download via Service Portal
- 🛠️ Station Manager tools for master-data maintenance & gate validation
- 📊 Metro Operations dashboards (ticket volume, revenue, peak-time analytics)
- ⚙️ IT Admin configuration of catalog variables, fare rules, and ACLs — no code required

---

## 🏗️ Technology Stack

| Layer | Technology / Component |
|---|---|
| **Presentation** | ServiceNow Service Portal, UI Pages, WhatsApp Business Chatbot |
| **Application / Process** | Service Catalog, Flow Designer, Business Rules, Script Includes, Catalog Client Scripts |
| **Integration** | Integration Hub, REST/SOAP APIs, Payment Gateway (UPI/Card/Wallet), QR Code Generation Library |
| **Data** | Custom Tables — Station Master, Fare Rule Table, Ticket/QR Records, Transaction Logs |
| **Notification** | Email, SMS Gateway, Push Notifications, WhatsApp Business API |
| **Reporting & Analytics** | Performance Analytics, Reports, Dashboards |
| **Security & Administration** | Access Control Lists (ACLs), OAuth 2.0, Data Encryption, Role-based Views |

The solution runs entirely on the **Now Platform**, using out-of-the-box Service Portal for the front end and Integration Hub spokes for all third-party connections — keeping the footprint minimal and serving all personas from a single, centrally administered system.

---

## 👥 Actors & Roles

| Actor | Role |
|---|---|
| **Passengers** | Book tickets, make payments, receive & use QR tickets, view booking history |
| **Station Managers** | Maintain station/fare master data, validate QR tickets at gates, monitor station-level ticket volume |
| **Metro Operations Team** | Consume analytics/reports, manage exceptions, plan schedules based on demand |
| **IT Admins** | Configure catalog variables, ACLs, and integration endpoints |

---

## 📋 Requirements Summary

**Functional:** Ticket booking, fare calculation, payment processing, QR ticket generation, notifications, administration & reporting.

**Non-Functional:**
- ⚡ Fare calculation & QR generation within 3 seconds of payment confirmation
- 📈 Handles concurrent booking spikes during peak hours
- 🟢 99.5% uptime target during metro operating hours
- 🔒 PCI-compliant payment handling, ACL-governed sensitive tables
- 🧭 Booking completable in under 5 steps, mobile-friendly UI
- 🧾 Full audit trail with timestamp & correlation ID on every event
- 🔧 Fare rules/station data configurable without code deployment

---

## 📂 Project Structure

```
ServiceNow Project/
├── 1. Ideation Phase/
│   ├── Problem Statement
│   ├── Empathy Map Canvas
│   └── Brainstorming & Idea Prioritization
├── 2. Requirement Analysis/
│   ├── Customer Journey Map
│   ├── Data Flow Diagram & User Stories
│   ├── Solution Requirements
│   └── Technology Stack
├── 3. Project Design Phase/
│   ├── Problem - Solution Fit
│   ├── Proposed Solution
│   └── Solution Architecture
├── 4. Project Planning Phase/
│   ├── Project Planning
│   └── Project Logic
├── 5. Project Development Phase/
│   ├── User Acceptance Testing
│   └── Performance Testing
├── 6. Project Documentation/
│   └── Functional Specification Document (FSD)
└── 7. Project Demonstration/
    └── Demo Video
```

---

## 🎥 Demo

A full walkthrough of the booking flow is available in `7. Project Demonstration/Demo_video.mp4`.

---

## 📖 Documentation

Detailed phase-wise documentation (ideation, requirements, design, planning, testing, and FSD) is available inside the respective folders in this repository.
