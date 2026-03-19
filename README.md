# 🛍️ sanctions.io — Shopify App Demo (Compliance SaaS Integration)

## 🚀 Overview
This is a **demo Shopify Embedded App** that simulates a full compliance SaaS integration flow for eCommerce merchants.

The goal of this demo is to showcase:
- Install → Account Provisioning → Live Screening
- Zero manual onboarding
- Real-time compliance screening workflows inside Shopify

This demo is **frontend-driven with simulated backend logic**, designed to demonstrate product thinking, architecture, and UX for a production-grade Shopify App.

---

## 🎯 Key Capabilities

### ✅ 1. Install → Automated Provisioning
- Simulated Shopify OAuth flow
- Automatic account creation
- API key generation
- Webhook registration
- Trial activation (30 days)

➡️ No manual setup required — merchant is ready instantly

---

### ✅ 2. Embedded App UI (Shopify-style)
- Sidebar navigation (App Bridge style)
- Clean Polaris-inspired UI
- Fully interactive panels

---

### ✅ 3. Dashboard (Analytics + Activity)
- Total screenings
- Hits detected
- False positives
- Clear passes
- Activity feed
- Screening volume chart

---

### ✅ 4. Manual Screening
- Input: Name, Country, DOB, Entity type
- Simulates sanctions screening (OFAC, EU, UN, etc.)
- Detects high-risk entities (e.g. Vladimir Putin)
- Shows:
  - Match result
  - Risk level
  - Entity details
- Actions:
  - Mark false positive
  - Escalate

---

### ✅ 5. Order Screening (Webhook Simulation)
- “Simulate Order” triggers screening
- Async processing (queue-like behavior)
- Updates UI in real time
- Displays:
  - Order status
  - Risk level
  - Screening results

---

### ✅ 6. Webhook Logs
- Simulates Shopify webhooks:
  - orders/create
  - customers/create
  - app/uninstalled
- Real-time event logging
- Displays payload + result

---

### ✅ 7. API & Account Management
- Auto-generated API key
- Account ID
- Copy / show key
- REST API usage example

---

### ✅ 8. Settings Panel
- Auto-screening toggles
- Fuzzy matching
- PEP screening
- Sensitivity threshold
- Notifications

---

### ✅ 9. Billing Simulation
- Plan selection UI
- Starter / Professional tiers
- Shopify Billing API simulation

---

## 🧠 Architecture (Conceptual)

### Frontend
- HTML, CSS, Vanilla JS
- Polaris-inspired design system
- Shopify embedded app UX

### Backend (Simulated)
- OAuth flow (mocked)
- Account provisioning API
- Screening API
- Webhook handlers

### Data Handling
- In-memory storage:
  - merchants
  - screenings
  - orders
  - webhook logs

---

## 🔄 Core Flow (End-to-End)

1. User clicks **Install App**
2. OAuth simulation completes
3. System:
   - Creates account
   - Generates API key
   - Registers webhooks
4. Redirect to dashboard
5. Merchant can:
   - Run manual screenings
   - Process orders automatically
   - View logs and analytics

---

## 🧪 Demo Scenarios to Try

### 1. High-Risk Match
- Go to Manual Screening
- Enter: `Vladimir Putin`
- See: High-risk sanctions hit

### 2. Order Screening Flow
- Go to Order Screening
- Click “Simulate Order” multiple times
- Observe:
  - Async processing
  - Risk detection
  - Dashboard updates

### 3. Webhook Activity
- Open Webhook Logs
- Watch real-time event entries

---

## ⚙️ How to Run

1. Download the repository
2. Open the HTML file in your browser:

```bash
sanctions-shopify-demo.html
```

No setup required — runs locally

---

## 🏗️ Production Implementation Plan

To convert this demo into a real Shopify App:

### Shopify Layer
- GraphQL Admin API
- OAuth authentication
- App Bridge + Polaris

### Backend
- Node.js (Express / NestJS)
- Secure token storage
- API key mapping

### Queue System
- Redis + BullMQ
- Retry + idempotency handling

### Database
- PostgreSQL
- Tables:
  - merchants
  - api_keys
  - screenings
  - webhook_events

### Infrastructure
- Hosting: Railway / Fly.io / Render
- Monitoring: Sentry + Logs
- DB: Supabase / Neon

---

## 🔐 Compliance Considerations

- GDPR webhook support:
  - customers/data_request
  - customers/redact
  - shop/redact

- Secure API key storage
- Encrypted tokens
- Audit logs for screenings

---

## ⚠️ Disclaimer

This is a **demo project only**:
- No real Shopify API integration
- No real sanctions API calls
- No persistent database

Built purely for:
- Demonstration
- Prototyping
- Client validation

---

## 💡 Future Enhancements

- Real Shopify OAuth integration
- Live sanctions API connection
- Shopify Flow integration
- POS & B2B support
- Advanced risk scoring engine

---

## 📌 Summary

This demo demonstrates:
- Strong understanding of Shopify app architecture
- Real-world SaaS integration patterns
- Event-driven screening workflows
- Clean, embedded UX design

It is designed to move quickly from **concept → demo → production-ready system**.

---

## 🤝 Contact

If you're reviewing this demo and want to take it to production, feel free to connect.
