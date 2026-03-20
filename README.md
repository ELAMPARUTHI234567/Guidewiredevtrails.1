<div align="center">

<img src="https://img.shields.io/badge/📦-ShieldRoute-FF6B35?style=for-the-badge&labelColor=0D1B2A&color=FF6B35" height="40"/>

# ShieldRoute — Parametric Income Insurance for India's Gig Economy

> *"When warehouses shut and routes freeze, your weekly paycheck shouldn't vanish with them."*

[![Hackathon](https://img.shields.io/badge/Guidewire-DEVTrails%202026-FF6B35?style=flat-square&logo=data:image/svg+xml;base64,)](https://guidewire.com)
[![Persona](https://img.shields.io/badge/Persona-Amazon%20Flex%20%2F%20Flipkart-0D1B2A?style=flat-square)](/)
[![Coverage](https://img.shields.io/badge/Coverage-Income%20Loss%20Only-02C39A?style=flat-square)](/)
[![Pricing](https://img.shields.io/badge/Pricing-Weekly%20Model-028090?style=flat-square)](/)
[![Platform](https://img.shields.io/badge/Platform-Web%20PWA-9C27B0?style=flat-square)](/)

**Phase 1 Submission — Ideation & Foundation**

[📋 Problem Statement](#-problem-statement) · [💡 Our Solution](#-our-solution) · [👤 Persona](#-persona--arjun-sharma) · [⚡ Triggers](#-parametric-triggers) · [🤖 AI/ML](#-aiml-architecture) · [💰 Pricing](#-weekly-premium-model) · [🏗️ Tech Stack](#️-tech-stack) · [👥 Team](#-team)

</div>

---

## 📋 Problem Statement

India's platform-based delivery partners (Amazon Flex, Flipkart Hub) are the backbone of the digital economy. External disruptions — extreme weather, pollution, natural disasters, curfews, and warehouse shutdowns — can reduce their working hours and cause them to **lose 20–30% of their monthly earnings**.

Currently, gig workers have **zero income protection** against these uncontrollable events. When disruptions occur, they bear the full financial loss with no safety net.

| Metric | Reality |
|--------|---------|
| Average disruption days/year | 10–15 days |
| Annual unprotected income loss | ₹6,000 – ₹12,000 |
| Insurance products for e-commerce delivery | **Zero** |
| Days to receive any compensation | **Never** |

---

## 💡 Our Solution

**ShieldRoute** is an AI-powered **parametric income insurance platform** built exclusively for Amazon Flex and Flipkart Delivery Hub partners.

### The Core Idea

ShieldRoute is a **parametric income insurance platform** — meaning payouts are triggered automatically by measurable external events, not by workers filing claims. When a verified disruption crosses a defined threshold in a delivery partner's active zone, the system pays them directly to their UPI account.

> **No forms. No phone calls. No waiting.**

### Why E-Commerce Delivery Partners Specifically

Food delivery workers face gradual slowdowns in bad weather — fewer orders, lower earnings. But Amazon Flex and Flipkart Hub partners work on **confirmed block-based shifts**. One disruption wipes the entire block — it's binary. You either work the block or you don't.

| Factor | Food Delivery (Swiggy/Zomato) | E-Commerce (Amazon/Flipkart) |
|--------|-------------------------------|-------------------------------|
| Income model | Per-order, flexible | Block-based — all or nothing |
| Zone flexibility | High — can move around | Low — zone-locked, hub-dependent |
| Disruption impact | Gradual slowdown | Entire block cancelled = ₹0 |
| Warehouse dependency | None | HIGH — hub closure = zero income |
| Days at full zero income | Rare | 12–15 per year |

This **all-or-nothing income structure** makes parametric insurance far more valuable and far more precise for this persona.

> ⚠️ **Coverage Scope:** Income Loss ONLY — not vehicles, not health, not accidents.
> ⚠️ **Pricing Model:** Weekly basis — aligned to the Amazon/Flipkart payment cycle.

---

## 👤 Persona — Arjun Sharma

```
Name        : Arjun Sharma
City        : Pune (modeled for Delhi NCR, Bengaluru, Hyderabad, Kolkata)
Platform    : Amazon Flex / Flipkart Delivery Hub
Work model  : Block-based shifts (3–6 hr blocks, 1–3 blocks/day)
Daily income: ₹700 – ₹1,100 on active days
Weekly income: ₹4,200 – ₹5,800
Risk type   : Zone-locked routes, hub-dependent, long outdoor exposure
Insurance   : None — has never accessed income protection
```

### Persona-Based Scenarios

**Scenario 1 — Flash Flood (Environmental)**
> Heavy rainfall in Pune's Hadapsar zone exceeds 50mm in 4 hours. Amazon suspends Arjun's delivery block. ShieldRoute detects the IMD/Open-Meteo trigger, validates his zone, triggers ₹850 payout to his UPI in 20 minutes. Arjun gets a WhatsApp: *"₹850 credited — stay safe."*

**Scenario 2 — Hub Shutdown (Operational ★ Unique)**
> A fire safety inspection forces Amazon's Bhiwandi fulfillment hub to shut for 8 hours. Workers cannot pick up packages. ShieldRoute's Hub Status Monitor detects the closure, cross-checks all confirmed blocks in that hub zone, and auto-initiates payouts for every affected worker simultaneously — zero individual action required.

**Scenario 3 — Section 144 / Curfew (Social)**
> A political event triggers Section 144 across 3 districts in UP. Traffic API shows near-zero mobility. ShieldRoute's Social Disruption Trigger fires, identifies all active Flipkart delivery partners with confirmed blocks in those zone IDs, and processes compensations within 30 minutes.

**Scenario 4 — Extreme Heat (Environmental)**
> Delhi hits 46°C. DM issues a heat advisory suspending outdoor labour between 11 AM–4 PM. Amazon Flex suspends morning blocks. Workers receive partial payout of ₹420 (50% of avg daily block rate).

**Scenario 5 — Severe AQI (Environmental)**
> AQI crosses 400 in North Delhi during Diwali. Amazon reduces deliveries per CPCB compliance. ShieldRoute detects the OpenAQ spike, identifies impacted workers, initiates proportional payouts.

---

## 💡 Application Workflow

```
┌────────────────────────────────────────────────────────────────────────────┐
│                        SHIELDROUTE PLATFORM FLOW                           │
│                                                                            │
│  [ONBOARDING]       [POLICY]          [MONITOR]          [PAYOUT]         │
│                                                                            │
│  Worker registers → AI Risk Score → 5 live disruption → Auto UPI          │
│  Name, City,         calculated       triggers polling    payout +         │
│  Platform ID,        Weekly premium   every 15 mins      WhatsApp alert   │
│  Hub Zone,           quoted &                                              │
│  Block Rate,         accepted                                              │
│  UPI ID                                                                    │
│                                                                            │
│       ↑ ML Premium Model                    ↑ Fraud Engine                │
│    XGBoost on zone risk,            GPS zone validation,                   │
│    hub history, seasonality         block confirmation check,              │
│                                     velocity + anomaly detection           │
└────────────────────────────────────────────────────────────────────────────┘
```

### Step-by-Step User Journey

1. **60-Second Onboarding** — Worker enters name, city, delivery platform, hub zone pin code, typical daily block rate, and UPI ID. DigiLocker-lite mock for Aadhaar verification.
2. **AI Risk Profile Generated** — ML model scores the worker's hub zone and delivery pattern.
3. **Weekly Policy Issued** — One-tap acceptance. Auto-debit every Monday from UPI.
4. **Continuous Silent Monitoring** — 5 trigger sources polled every 15 minutes. Worker does nothing.
5. **Trigger Fires Automatically** — System cross-validates against worker's confirmed block status and zone.
6. **Fraud Validation (AI)** — GPS zone match, block confirmation, duplicate check, velocity rules — under 60 seconds.
7. **Payout + Notification** — UPI transfer initiated. Worker notified on WhatsApp/SMS.
8. **Dashboard Access** — Coverage history, earnings protected, zone risk forecast.

---

## ⚡ Parametric Triggers

All triggers operate at **pin code → 5km delivery zone polygon** level — not city-wide — to eliminate false positives.

| # | Trigger | Data Source | Threshold | Payout |
|---|---------|-------------|-----------|--------|
| 🌧️ 1 | Flash Flood / Heavy Rain | Open-Meteo API (free) + IMD | Rainfall >45mm in 4hrs in delivery zone | 80–100% of daily avg block rate |
| 🌡️ 2 | Extreme Heat Advisory | Open-Meteo + Gov Advisory Mock | Temperature >43°C OR official advisory issued | 50–70% of daily avg |
| 🌫️ 3 | Severe AQI Alert | OpenAQ API (free) | AQI >350 in delivery zone | 40–60% of daily avg |
| 🚧 4 | Curfew / Social Shutdown | Mobility Index API (mock) | Zone mobility index <20% of normal | 70–100% of daily avg |
| 🏭 5 | **Hub / Warehouse Closure ★** | Platform Ops Status API (mock) | Hub tagged "Closed / Suspended" >2hrs during active block window | **100% of confirmed block rate** |

> **Trigger 5 is our key differentiator.** No food delivery insurance product can address warehouse/hub shutdowns — a risk unique to e-commerce that wipes out entire confirmed blocks simultaneously.

### Payout Formula

```
Block Payout = Worker's Avg Block Rate × Disruption Severity % × (Blocked Hours / Total Scheduled Hours)

Daily Cap    = 1.5 × Worker's Avg Daily Block Rate
Weekly Cap   = Policy Tier Maximum (₹1,800 / ₹3,000 / ₹5,000)

Example (Flood Scenario):
  Worker avg daily block rate : ₹900
  Trigger                     : Flash flood, severity 90%, full-day block cancelled
  Payout = ₹900 × 90% × (8/8) = ₹810
```

---

## 🤖 AI/ML Architecture

### 1. Dynamic Weekly Premium Model

The XGBoost premium pricing model recalculates every worker's weekly premium each Monday using:

- Zone's historical flood and heat risk score
- Seasonal forecast for the coming week
- Worker platform tenure and loyalty
- Block confirmation consistency rate
- 7-day weather disruption probability

A loyal worker in a low-risk zone pays ₹29/week. A new worker in a flood-prone Chennai neighbourhood pays ₹79/week.

```
Algorithm    : XGBoost Regression
Training Data: 50,000 synthetic records from IMD rainfall (2019–2024), CPCB AQI, hub closure data
Output       : Weekly premium (₹19–₹99) + coverage tier assignment + risk band label
Retraining   : Simulated weekly batch job via MLflow
```

### 2. Intelligent Fraud Detection Engine

The Isolation Forest fraud detection engine validates every trigger event before a payout fires.

| Fraud Vector | Detection Method |
|---|---|
| GPS zone spoofing | Cross-validate platform last-location vs. trigger zone — delta >10km → flag |
| Fake block confirmation | Block status lookup via Platform API mock — unconfirmed blocks ineligible |
| Duplicate claim | Device fingerprint + UPI hash deduplication within trigger event window |
| Income inflation | Cross-check declared block rate vs. platform earnings history — outliers flagged |
| Velocity abuse | Max 2 trigger payouts per 7-day rolling window before human review |

Every fraud flag is explained using **SHAP values** — the insurer can see exactly why a claim was held, not just a score.

### 3. Predictive Risk & Insurer Intelligence Engine

The Prophet forecasting engine predicts next week's likely disruption probability per city zone and feeds that into the insurer's analytics dashboard alongside loss ratio projections.

```
Models Used    : Prophet (disruption forecast) + XGBoost Classifier (loss ratio)
Output         : 7-day zone risk map, predicted payout volume vs. premium collected
Dashboard      : Chloropleth heatmap, cohort analysis by city × tenure × risk tier
```

---

## 💰 Weekly Premium Model

### Why Weekly, Not Monthly

Amazon Flex and Flipkart both pay their partners weekly. ShieldRoute's premium auto-debits from the worker's UPI **every Monday — the same morning the platform earnings arrive**. The worker pays ₹29–₹79 from the money they just received, before they even notice it. This removes the psychological friction of monthly insurance premiums.

### Premium Tiers

| Tier | Zone Risk Profile | Weekly Premium | Weekly Coverage Cap | % of Income |
|------|-------------------|---------------|---------------------|-------------|
| 🟢 Low Risk | Stable hub, non-flood zone | ₹29 / week | ₹1,800 / week | ~1.1% |
| 🟡 Moderate | Seasonal weather exposure | ₹49 / week | ₹3,000 / week | ~1.4% |
| 🔴 High Risk | Flood-prone / heat-stressed / bandh-frequent zone | ₹79 / week | ₹5,000 / week | ~1.8% |

> For a worker earning ₹4,500/week, the product costs less than **two cups of chai** to protect most of their income.

Premiums are **recalculated every Monday** using fresh ML inference — zone risk, seasonal forecast, worker tenure, and block history.

---

## 🔴 What ShieldRoute Strictly Excludes

The problem statement has a hard constraint — ShieldRoute never touches these:

| ❌ Excluded | Reason |
|------------|--------|
| Vehicle repairs or maintenance | Personal mechanical failure, not an external parametric trigger |
| Health, accident, or life insurance | Out of coverage scope |
| Fuel surcharges or commission changes | Platform policy decisions, not external disruptions |
| Voluntary absence | Worker choice, not uncontrollable event |
| Long-term platform rate changes | Structural business decision, not a zone-level event |

The system only pays when an **external, measurable, zone-level event** causes income loss that the worker had no control over.

---

## 🖥️ Platform Choice — Web PWA

We chose a **Progressive Web App (PWA)** over a native mobile app:

| Factor | Reasoning |
|--------|-----------|
| No App Store barrier | Workers access via WhatsApp link — no Play Store download |
| Low-end device support | Works on ₹6,000 Android phones with 1–2GB RAM |
| Insurer admin panel | Desktop-first analytics dashboard — web is the natural fit |
| Instant updates | All workers see the same live build without reinstalling |
| Offline resilience | Service workers cache policy status and last payout record |
| Hackathon velocity | Single codebase, faster iteration within our 6-week timeline |

---

## 🏗️ Tech Stack

### Frontend — React Web App (PWA)

```
React 18 + TypeScript
Tailwind CSS              — mobile-responsive, low-end Android browser support
Leaflet.js                — zone mapping, hub locations, GPS visualization
Recharts                  — worker dashboard + insurer analytics charts
React Query               — API state management
PWA (Service Worker)      — offline policy/payout status access
```

### Backend — Python + Node.js

```
FastAPI (Python)          — core REST API, trigger engine, ML inference
Node.js + Express         — Razorpay payment webhook handler
PostgreSQL                — workers, policies, claims, payouts, audit log
Redis                     — trigger event queue, real-time zone status cache
Celery + Beat             — scheduled trigger polling every 15 minutes
```

### AI / ML Stack

```
scikit-learn + XGBoost    — premium pricing model
Isolation Forest          — fraud anomaly detection
Prophet                   — weekly disruption forecasting
MLflow                    — experiment tracking + model registry
SHAP                      — fraud flag explainability
Pandas + NumPy            — feature engineering pipeline
```

### External API Integrations

```
Open-Meteo API (free)         — real-time weather + 7-day forecast
OpenAQ API (free)             — AQI by coordinates
IMD Open Data                 — historical rainfall (model training)
Google Mobility API (mock)    — curfew / social disruption detection
Platform Ops API (mock)       — hub status, block confirmation lookup
Razorpay Sandbox              — UPI payout simulation
Twilio (free tier)            — WhatsApp + SMS notifications
DigiLocker API (mock)         — worker identity verification
```

### Infrastructure

```
Docker + Docker Compose   — local dev environment
Render / Railway          — free-tier cloud deployment for demo
GitHub Actions            — CI/CD (lint → test → deploy)
```

---

## 📁 Repository Structure

```
shieldroute/
├── frontend/
│   └── src/
│       ├── pages/
│       │   ├── Onboarding.tsx       — Worker registration + KYC
│       │   ├── Dashboard.tsx        — Worker: coverage, payouts, forecast
│       │   ├── Policy.tsx           — Weekly policy management
│       │   ├── Claims.tsx           — Auto-generated claim history
│       │   └── AdminPanel.tsx       — Insurer: analytics + fraud queue
│       ├── components/              — ZoneMap, PayoutCard, RiskBadge, etc.
│       └── hooks/                   — API hooks, auth, geolocation
├── backend/
│   ├── api/                         — FastAPI route handlers
│   ├── ml/
│   │   ├── premium_model.py         — XGBoost weekly premium calculator
│   │   ├── fraud_detection.py       — Isolation Forest + rule engine
│   │   └── risk_forecast.py         — Prophet disruption forecasting
│   ├── triggers/
│   │   ├── weather_trigger.py       — Rain + heat (Open-Meteo)
│   │   ├── aqi_trigger.py           — Pollution (OpenAQ)
│   │   ├── heat_trigger.py          — Extreme temperature
│   │   ├── social_trigger.py        — Curfew / mobility shutdown
│   │   └── hub_closure_trigger.py   — ★ E-commerce unique trigger
│   ├── payments/                    — Razorpay sandbox UPI payout
│   └── notifications/               — Twilio WhatsApp + SMS
├── data/
│   ├── synthetic_workers.csv        — Worker profile training data
│   ├── zone_risk_scores.json        — Pre-computed zone risk table
│   └── historical_triggers.csv      — Synthetic disruption event log
├── docs/
│   ├── architecture.png
│   └── api_spec.yaml
├── docker-compose.yml
└── README.md
```

---

## 🗓️ Development Plan

### ✅ Phase 1 (Mar 4–20): Ideation & Foundation — *Current Phase*

- [x] Persona definition: Amazon/Flipkart e-commerce delivery partner
- [x] 5 real-world scenario definitions
- [x] Weekly premium model formula + tier structure finalized
- [x] 5 parametric triggers + data sources identified
- [x] ML architecture planned (XGBoost + Isolation Forest + Prophet)
- [x] Tech stack finalized
- [x] GitHub repository with this README
- [ ] Onboarding flow wireframe (Figma)
- [ ] FastAPI project scaffold + Docker setup
- [ ] Synthetic training dataset generated
- [ ] Premium model v0 trained + validated on synthetic data

### Phase 2 (Mar 21 – Apr 4): Automation & Protection

- [ ] Worker onboarding + policy creation (React)
- [ ] 5 automated triggers live (3 real APIs + 2 mocks)
- [ ] Dynamic premium engine integrated end-to-end
- [ ] Zero-touch auto-claim pipeline (trigger → validate → payout)
- [ ] Fraud detection v1: GPS validation + block check + velocity rules
- [ ] Basic worker dashboard (active policy, payout history)
- [ ] Phase 2 demo video (2 min)

### Phase 3 (Apr 5–17): Scale & Optimise

- [ ] Advanced fraud detection (Isolation Forest + income inflation detection)
- [ ] Full Razorpay sandbox UPI payout flow
- [ ] Insurer admin panel (loss ratio, fraud queue, zone heatmap, forecast)
- [ ] Worker dashboard v2 (earnings protected YTD, zone risk forecast)
- [ ] Hindi + regional language notification templates
- [ ] Trigger-to-payout latency < 60s end-to-end
- [ ] Final 5-min demo video: simulated flood trigger → auto payout walkthrough
- [ ] Final pitch deck (PDF)

---

## 🌟 Why ShieldRoute Wins

| Feature | Why It Matters |
|---------|----------------|
| **Hub Closure Trigger ★** | No other income insurance product addresses warehouse shutdowns — a risk unique to e-commerce that wipes out entire confirmed blocks |
| **Block-Rate Precision Payouts** | Payouts match the worker's actual confirmed block rate — not a city average |
| **Binary Loss Architecture** | Payout model acknowledges e-commerce workers lose entire blocks, not fractions of income |
| **Monday Auto-Debit Alignment** | Premium timed to debit on the same day workers receive Amazon/Flipkart weekly payment |
| **Zero Claims Experience** | The average Amazon Flex partner never touches a "claim" button — the system does everything |
| **SHAP-Explainable Fraud Scores** | Insurer sees exactly *why* a claim was flagged — no black box decisions |
| **Pin-Code Precision** | 5km zone polygon triggers — not city-wide alerts that cause false payouts |

---

## 📎 Submission Links

| Item | Link |
|------|------|
| 🎥 Phase 1 Demo Video (2 min) | *[Add before March 20]* |
| 🔗 Live Demo | *[Add link]* |
| 💻 GitHub Repository | *[This repo URL]* |
| 📊 Pitch Deck | *[Add PDF link]* |

---

## 👥 Team

| Name | Role |
|------|------|
| 🟢 Om Ganesh E P | Full Stack + Backend (FastAPI, PostgreSQL) |
| 🔵 Nivetha R | ML / AI Engineering (XGBoost, Fraud Detection) |
| 🟣 Yuvanraj B | Frontend + UX (React PWA, Dashboards) |

---
<img width="1123" height="305" alt="image" src="https://github.com/user-attachments/assets/af335b87-8ac4-4461-a5bd-9b7e49440d9c" />
<img width="1105" height="513" alt="Screenshot 2026-03-20 230029" src="https://github.com/user-attachments/assets/5699d1d8-ffc9-4f4d-89ff-ff52d6863090" />
<img width="1133" height="293" alt="Screenshot 2026-03-20 230057" src="https://github.com/user-attachments/assets/5797c21f-6e99-437e-be8c-4d34f68060ab" />

<img width="1123" height="305" alt="Screenshot 2026-03-20 230116" src="https://github.com/user-attachments/assets/1725a3a0-3f92-4865-ac24-a9b326961336" />



<div align="center">

*Built with purpose for India's 8 million e-commerce delivery partners*

**Guidewire DEVTrails 2026 · University Hackathon**

`Weekly pricing` · `Pin-code precision` · `AI-validated payouts` · `Hub Closure trigger (unique)`

</div>

demo video:

https://drive.google.com/file/d/1qY-HrVKuXGQcrldZOIH9WEhZRIdmyIsD/view?usp=sharing

dashboard prototype link:

https://elamparuthi234567.github.io/shieldroute.0/

