<div align="center">

# GigSaathi

### AI-Powered Parametric Insurance for Gig Workers — Phase 1

[![Phase](https://img.shields.io/badge/Phase-1%20Ideation-blue?style=for-the-badge)](https://github.com)
[![Platform](https://img.shields.io/badge/Platform-Android%20%2B%20Web-green?style=for-the-badge)](https://github.com)
[![AI](https://img.shields.io/badge/AI%2FML-Powered-red?style=for-the-badge)](https://github.com)
[![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](https://github.com)

**Android App** | **Admin Web** | **AI/ML Integration** | **Anti-Spoofing**

---

*Protecting gig workers' income from uncontrollable disruptions with fraud-proof, physics-based verification.*

> **Phase 1 — Ideation & Foundation**

</div>

---

## Table of Contents

- [Executive Summary](#executive-summary)
- [Persona and Market Analysis](#persona-and-market-analysis)
- [Core Problem Statement](#core-problem-statement)
- [Adversarial Defense and Anti-Spoofing Strategy](#adversarial-defense-and-anti-spoofing-strategy)
- [Platform Strategy](#platform-strategy)
- [Weekly Premium Model](#weekly-premium-model)
- [Parametric Triggers](#parametric-triggers)
- [AI and ML Integration](#ai-and-ml-integration)
- [Technical Architecture](#technical-architecture)
- [Development Roadmap](#development-roadmap)
- [Risk Assessment and Mitigation](#risk-assessment-and-mitigation)
- [Success Metrics](#success-metrics)
- [Appendix](#appendix)

---

## Executive Summary

GigSaathi is an AI-powered parametric insurance platform designed exclusively for food delivery partners (Zomato, Swiggy). We protect their daily income from uncontrollable external disruptions — severe weather, unplanned curfews, and sudden market closures — that cause immediate loss of wages.

### Market Opportunity

| Metric | Value |
|:---|:---|
| Active Delivery Partners (India) | 2.1 Million+ |
| Avg. Loss per Disruption | Rs. 500 – Rs. 1,500 |
| Target Market (Food Delivery) | 1.2 Million |
| Weekly Premium | Rs. 49 – Rs. 147 |
| Payout per Event | Rs. 300 – Rs. 500 |

### What We Built

| Feature | Description |
|:---|:---|
| Multi-Layer Fraud Detection | 7+ telemetry streams to detect GPS spoofing |
| Physics-Based Validation | Wi-Fi fingerprinting + barometric pressure + motion analysis |
| Graph-Based Ring Detection | Identifies coordinated 500-worker fraud syndicates |
| Graduated UX | Auto-payout for honest workers, verification for suspicious claims |
| Weekly Pricing | Aligns with gig workers' cash flow cycles |

### How We Compare

```
Traditional Insurance          GigSaathi
───────────────────            ─────────────────
 - Monthly premiums             - Weekly pricing
 - Manual claims                - Parametric auto-triggers
 - Weeks to payout              - 30-second payouts
 - No fraud detection           - 7-layer anti-spoofing
 - Single data point (GPS)      - 12+ telemetry streams
 - No collusion detection       - Graph-based ring detection
```

---

## Persona and Market Analysis

### Primary Persona: Ramesh, Food Delivery Partner

| Attribute | Details |
|:---|:---|
| Age | 22–28 years |
| Platform | Zomato / Swiggy |
| Daily Earnings | Rs. 600 – Rs. 1,200 |
| Work Pattern | 8–10 hours/day, 6 days/week |
| Primary Zones | Restaurant clusters within 3–5 km radius |
| Device | Mid-range Android (Rs. 8,000 – Rs. 15,000) |
| Pain Points | No income during rains, market closures, app crashes |
| Trust Factors | Instant payouts, minimal documentation, no premium when not working |

### Market Segmentation

```
                    Total Delivery Partners (India)
                              2.1 Million
                                  |
        +--------------------------+--------------------------+
        |                          |                          |
   Food Delivery            E-commerce              Grocery/Q-Commerce
  Zomato / Swiggy         Amazon / Flipkart          Zepto / Blinkit

    1.2 Million              0.6 Million              0.3 Million
    [TARGET]                Future Phase              Future Phase
```

### Why Food Delivery First?

| Reason | Explanation |
|:---|:---|
| Highest Disruption Exposure | Rain = 40% order surge, but also 60% delivery partner dropout |
| Standardized Patterns | Consistent work zones and timing enables accurate risk modeling |
| Platform Integration | Zomato/Swiggy have mature APIs for partner verification |
| Fraud History | Documented cases of collusion rings as highlighted in the crisis scenario |

---

## Core Problem Statement

### The Crisis

A sophisticated syndicate of 500 delivery workers successfully exploited a beta parametric insurance platform. Using GPS-spoofing apps and coordinated Telegram groups, they triggered mass false payouts while resting at home — instantly draining the liquidity pool.

### The Vulnerability

Simple GPS verification is obsolete. Fraudsters can fake their location, but they **cannot fake reality.**

### Our Solution: 3-Layer Defense

```
                    +-------------------------------------+
                    |         HONEST WORKER               |
                    |         Auto-approve                |
                    |         Payout in 30 seconds        |
                    +----------------+--------------------+
                                     |
        +----------------------------+----------------------------+
        |                            |                            |
        v                            v                            v
+-------------------+     +-------------------+     +-------------------+
|    GREEN ZONE     |     |    YELLOW ZONE    |     |     RED ZONE      |
|   Score: 0-30     |     |   Score: 31-70    |     |   Score: 71-100   |
|                   |     |                   |     |                   |
|   Auto-payout     |     |   Soft Hold       |     |   Hard Hold       |
|   Instant         |     |   2-hour delay    |     |   Selfie / Live   |
|   No friction     |     |   SMS: "Reserved" |     |   SMS: "Verify"   |
+-------------------+     +-------------------+     +-------------------+
```

---

## Adversarial Defense and Anti-Spoofing Strategy

### 1. Differentiating Genuine from Spoofed Claims

Our architecture uses multi-modal behavioral fingerprinting to distinguish genuine distress from coordinated fraud across three layers.

#### A. Temporal-Spatial Consistency

| Indicator | Genuine Stranded Worker | GPS Spoofer |
|:---|:---|:---|
| Velocity | Gradual deceleration before event | Instant teleportation at impossible speeds |
| Location Path | Follows road networks, last known near delivery zones | Direct jump from home to flood zone |
| Time Correlation | Arrival time consistent with weather progression | Claim timing inconsistent with last known location |

#### B. Sensor Fusion (The Physics Layer)

```
+-----------------------------------------------------------------------------+
|                      DEVICE TELEMETRY COLLECTION                            |
+-----------------------------------------------------------------------------+
|                                                                             |
|   GPS Coordinates              Wi-Fi BSSID Fingerprint                      |
|   Barometric Pressure          Accelerometer / Gyroscope                    |
|   Battery Drain Rate           IP Address & Cell Tower                      |
|   Ambient Light                Bluetooth Devices Nearby                     |
|   Step Count                   Device Orientation                           |
|   Screen On/Off Status         Charging State                              |
|                                                                             |
+-----------------------------------------------------------------------------+
```

A spoofer can fake GPS, but cannot fake:

| Check | Description |
|:---|:---|
| Wi-Fi Networks | The networks visible at their actual location |
| Barometric Pressure | Readings matching weather API data |
| Motion Patterns | Being "stranded" vs. phone sitting on a table |
| Network Latency | Response time to regional servers |

#### C. Graph-Based Collusion Detection

For syndicate attacks, we use community detection algorithms:

```
500-Worker Ring Detection Flow
------------------------------------------------------------------

Step 1 -> Identify devices sharing identical spoofed trajectories
          Flag: 50+ accounts with identical movement patterns

Step 2 -> Detect temporal clustering
          Flag: 100+ claims from same coordinates within 3 minutes

Step 3 -> Social graph analysis (Telegram groups, referral codes)
          Flag: Users connected through known fraud networks

Step 4 -> IP / Network fingerprint correlation
          Flag: 20 accounts sharing same VPN endpoint

Step 5 -> Automatic circuit breaker activation
          Pause payouts only for the anomalous cluster
```

---

### 2. Data Signals Beyond GPS

| Category | Data Points | Fraud Signal |
|:---|:---|:---|
| Device Fingerprint | Device ID, OS version, installed apps list | Multiple accounts on same device |
| Wi-Fi Fingerprint | Connected SSID, BSSID, nearby networks | Home network detected in flood zone |
| Barometric Pressure | hPa reading vs. weather API | 10+ hPa deviation from expected |
| Motion Analysis | Accelerometer X/Y/Z, stationary status | Phone flat on table while "stranded" |
| Network Telemetry | IP address, cell tower ID, VPN detection | IP geolocation mismatches GPS |
| Behavioral Biometrics | Typing cadence, swipe patterns | Bot-like automation patterns |
| Historical Baseline | 30-day work zones, typical hours | Claim from zone never worked before |

---

### 3. UX Balance: Protecting Honest Workers

| Risk Score | Action | Worker Experience |
|:---|:---|:---|
| 0–30 (Green) | Auto-approve, instant payout | "Rs. 450 credited to your account. Safe delivery!" |
| 31–70 (Yellow) | Soft hold with 2-hour delay | "We're verifying your location. Payout reserved. No action needed." |
| 71–100 (Red) | Hard hold + verification | "Quick verification needed. Send a selfie with your delivery bag." |

#### Safeguards for Honest Workers

| Safeguard | Description |
|:---|:---|
| False Positive Compensation | +Rs. 100 bonus if a flagged claim is later verified legitimate |
| Network Failure Grace | Offline claim recording with guaranteed payout upon connectivity |
| Whitelist Program | 6+ months clean history = bypass red flags entirely |
| 24/7 Human Review | 15-minute average response for appeals |

---

## Platform Strategy

### Android App (Delivery Partner)

95% of delivery partners use Android devices in the Rs. 8,000–Rs. 15,000 segment, making Android the priority platform.

#### Features

| Feature | Description |
|:---|:---|
| Quick Onboarding | 3-step registration: Phone OTP, KYC (Aadhaar/PAN), Platform verification |
| Telemetry SDK | Silent background collection of 12+ data points for fraud detection |
| One-Tap Claim | Single button to report disruption; system auto-fills location and time |
| Real-Time Status | Live feed of active policies, weather alerts, payout history |
| Offline Mode | Claims stored locally when network is down; auto-submit when online |
| Multi-Language | Hindi, English, Tamil, Telugu, Bengali, Marathi |

#### App Screen Flow

```
Splash Screen
     |
     v
Onboarding -----------------------------------------+
     |                                               |
     v                                               v
Phone Verification --------------------------> Platform Auth
     |                                         (Zomato/Swiggy)
     v                                               |
KYC Upload (Aadhaar/PAN) <--------------------------+
     |
     v
+--------------------------------------------------------------------+
|                         DASHBOARD                                   |
|---------------------------------------------------------------------|
|  Active Policy: Rs. 49/week                                         |
|  Current Coverage: Rs. 0 / Rs. 5,000                                |
|                                                                     |
|  Weather Alert: Heavy Rain Expected in your zone                    |
|                                                                     |
|  +---------------------------------------------------------------+  |
|  |                      CLAIM NOW                                |  |
|  +---------------------------------------------------------------+  |
|                                                                     |
|  Transaction History:                                               |
|  - Mar 19: Rs. 450 (Rain disruption)                                |
|  - Mar 15: Rs. 49 (Weekly premium)                                  |
+---------------------------------------------------------------------+
```

---

### Admin Web Application (Insurance Operations)

#### Modules

| Module | Purpose |
|:---|:---|
| Fraud Dashboard | Real-time alerts, risk maps, ring detection visualization |
| Claims Queue | Manual review interface for flagged claims |
| Risk Analytics | ML model performance, loss ratios, predictive trends |
| User Management | Whitelist/blacklist, policy adjustments |
| Payout Monitoring | Real-time liquidity tracking, fraud savings counter |

#### Admin Dashboard Layout

```
+-----------------------------------------------------------------------------+
|                    FRAUD DETECTION DASHBOARD                                |
+-----------------------------------------------------------------------------+
|                                                                             |
|  +--------------+ +--------------+ +--------------+ +--------------+       |
|  | Active       | | Avg Risk     | | Fraud        | | Saved        |       |
|  | Alerts       | | Score        | | Rings        | | Today        |       |
|  |     24       | |    0.68      | |     3        | | Rs. 24,500   |       |
|  +--------------+ +--------------+ +--------------+ +--------------+       |
|                                                                             |
|  +---------------------------------------------------------------------+   |
|  |                         LIVE RISK MAP                                |   |
|  |                                                                     |   |
|  |   [Interactive Map Showing High-Risk Zones]                         |   |
|  |                                                                     |   |
|  |   RED: 12 claims in Andheri East (possible ring detected)           |   |
|  |   YELLOW: 8 claims in Bandra (moderate risk)                        |   |
|  +---------------------------------------------------------------------+   |
|                                                                             |
|  +---------------------------------------------------------------------+   |
|  |                      ACTIVE FRAUD ALERTS                            |   |
|  +----------+------------+------------+----------+-------------------+ |   |
|  | Time     | User ID    | Claim ID   | Risk     | Anomalies         | |   |
|  +----------+------------+------------+----------+-------------------+ |   |
|  | 10:23 AM | user_***42 | claim_***12| 0.92 RED | Velocity, WiFi    | |   |
|  | 10:15 AM | user_***87 | claim_***45| 0.65 YLW | Pressure mismatch | |   |
|  | 10:02 AM | user_***23 | claim_***78| 0.88 RED | Ring detected     | |   |
|  +----------+------------+------------+----------+-------------------+ |   |
|                                                                             |
+-----------------------------------------------------------------------------+
```

---

## Weekly Premium Model

### Dynamic Pricing Formula

```
Weekly Premium = Base Rate x Risk Factor x Zone Multiplier x Trust Score

Where:
  Base Rate      : Rs. 49 (food delivery baseline)
  Risk Factor    : ML-predicted disruption probability (0.5x to 2.0x)
  Zone Multiplier: Hyperlocal weather/traffic risk (0.8x to 1.5x)
  Trust Score    : Behavioral reliability (0.7x to 1.0x)
```

### Example Pricing

| Scenario | Base | Risk | Zone | Trust | Final |
|:---|:---:|:---:|:---:|:---:|:---:|
| New user, safe zone, low risk week | Rs. 49 | 0.5x | 0.8x | 0.7x | **Rs. 14/week** |
| Regular user, moderate risk | Rs. 49 | 1.0x | 1.0x | 0.9x | **Rs. 44/week** |
| High-risk zone, monsoon week | Rs. 49 | 2.0x | 1.5x | 1.0x | **Rs. 147/week** |

### Coverage Benefits

| Benefit | Payout Amount | Frequency |
|:---|:---:|:---:|
| Weather Disruption (Rain, Flood, Heat Wave) | Rs. 500 per event | Max 2/week |
| Curfew / Strike | Rs. 400 per event | Max 1/week |
| App Crash (Platform outage) | Rs. 300 per event | Max 1/week |
| **Weekly Cap** | **Rs. 5,000** | — |

---

## Parametric Triggers

### Automated Event Detection

| Trigger | Data Source | Threshold | Payout |
|:---|:---|:---|:---:|
| Heavy Rain | Weather API (IMD) | >50mm in 3h OR >100mm in 24h | Rs. 500 |
| Flood Warning | Municipal + Weather API | Red alert issued for zone | Rs. 500 |
| Heat Wave | Weather API | >40 degrees C for 3 consecutive days | Rs. 500 |
| Curfew | Government API + News | Unplanned curfew announced | Rs. 400 |
| Zone Closure | Platform API | Market closed >2 hours | Rs. 400 |
| App Outage | Platform API (Zomato/Swiggy) | Service down >30 minutes | Rs. 300 |

### Trigger Workflow

```
+-----------------------------------------------------------------------------+
|                      PARAMETRIC TRIGGER PIPELINE                            |
+-----------------------------------------------------------------------------+
|                                                                             |
|  Weather API ----------+                                                    |
|                        |                                                    |
|  Government API -------+--> Event Detected --> Zone Affected?               |
|                        |         |                    |                      |
|  Platform API ---------+         |                    |                      |
|                                  v                    v                      |
|                          +---------------+    +---------------+             |
|                          | Auto-initiate |    | Push Notify   |             |
|                          | Claim for all |    | "Claim Ready" |             |
|                          | users in zone |    |               |             |
|                          +-------+-------+    +-------+-------+             |
|                                  |                    |                      |
|                                  +--------+-----------+                     |
|                                           v                                 |
|                              +-----------------------+                      |
|                              |   User Decision       |                      |
|                              |                       |                      |
|                              |  Accept Claim         |                      |
|                              |        OR             |                      |
|                              |  Decline and Work     |                      |
|                              +-----------------------+                      |
|                                                                             |
+-----------------------------------------------------------------------------+
```

---

## AI and ML Integration

### 1. Dynamic Premium Calculation

**Model:** XGBoost Regression with time-series features

```
Input Features:
  - Historical claims in zone (last 30 days)
  - Weather forecast (rain probability, temperature, wind)
  - Day of week, month, season
  - User's past claim frequency
  - Number of active policies in zone
  - Platform order volume trends

Output: Risk score (0-100) mapped to weekly premium multiplier
```

### 2. Fraud Detection Ensemble

**Model:** Stacked Ensemble (Random Forest + Isolation Forest + Neural Network)

```
+-----------------------------------------------------------------------------+
|                       FRAUD SCORING PIPELINE                                |
+-----------------------------------------------------------------------------+
|                                                                             |
|  Telemetry Data --> Feature Engineering                                     |
|         |              - Velocity features (speed, acceleration)            |
|         |              - WiFi consistency (SSID vs. location)               |
|         |              - Motion anomalies (stationary vs. claimed)          |
|         |              - Pressure deviation (sensor vs. weather)            |
|         |              - Historical deviation (zone, timing)                |
|         |                                                                   |
|         v                                                                   |
|  +---------------------------------------------------------------------+   |
|  |                      ENSEMBLE MODELS                                |   |
|  |                                                                     |   |
|  |  +------------------+    +------------------+                       |   |
|  |  |  Random Forest   |    |   Isolation      |                       |   |
|  |  |  (100 trees)     |    |   Forest         |                       |   |
|  |  +--------+---------+    +--------+---------+                       |   |
|  |           |                       |                                 |   |
|  |           +-----------+-----------+                                 |   |
|  |                       v                                             |   |
|  |  +----------------------------------------------------------+      |   |
|  |  |         Neural Network (3 layers, 128 units)              |      |   |
|  |  +----------------------------------------------------------+      |   |
|  |                       |                                             |   |
|  |                       v                                             |   |
|  |              Final Fraud Score (0-100)                              |   |
|  +---------------------------------------------------------------------+   |
|                                                                             |
+-----------------------------------------------------------------------------+
```

### 3. Graph-Based Ring Detection

**Algorithm:** DBSCAN Clustering + Louvain Community Detection

| Step | Description |
|:---|:---|
| Step 1 | Cluster claims by (latitude, longitude, timestamp) with DBSCAN |
| Step 2 | Build graph edges between users sharing device fingerprint, IP range, or group membership |
| Step 3 | Detect communities with Louvain algorithm |
| Step 4 | Flag communities with size > 10 and >80% high-risk claims |
| Step 5 | Trigger circuit breaker for the cluster |

### 4. Training and Deployment Timeline

| Phase | Activity |
|:---|:---|
| Week 1–2 | Collect synthetic telemetry data (simulated good + spoofed) |
| Week 3 | Train initial models on historical weather + claim data |
| Week 4 | A/B test fraud detection in production with 10% traffic |
| Week 5 | Full rollout with human review fallback |
| Week 6 | Retrain with real fraud data from production |

---

## Technical Architecture

### System Overview

```
+-----------------------------------------------------------------------------+
|                           GIGSAATHI PLATFORM                                |
+-----------------------------------------------------------------------------+
|                                                                             |
|  +-----------------------------+    +-------------------------------------+ |
|  |     ANDROID APP             |    |         ADMIN WEB                   | |
|  |     (Delivery Partner)      |    |         (Operations)                | |
|  +-----------------------------+    +-------------------------------------+ |
|  | Kotlin + MVVM               |    | React + TypeScript                  | |
|  | Room (Offline DB)           |    | MUI + TailwindCSS                   | |
|  | WorkManager (Telemetry)     |    | Mapbox GL (Risk Maps)               | |
|  | SafetyNet Attestation       |    | Recharts (Analytics)                | |
|  | Retrofit + OkHttp           |    | Socket.io (Real-time)               | |
|  +-------------+---------------+    +---------------+---------------------+ |
|                |                                    |                       |
|                +-----------------+------------------+                       |
|                                  |                                          |
|                                  v                                          |
|  +----------------------------------------------------------------------+  |
|  |                      API GATEWAY (Kong / NGINX)                       |  |
|  |                   Authentication | Rate Limiting | Routing            |  |
|  +----------------------------------------------------------------------+  |
|                                  |                                          |
|        +-------------------------+-------------------------+--------+      |
|        v                         v                         v        v      |
|  +------------+           +------------+           +--------+  +-------+   |
|  | PostgreSQL |           | TimescaleDB|           | Redis  |  | Neo4j |   |
|  |            |           |            |           |        |  |       |   |
|  | Users      |           | Telemetry  |           | Cache  |  | Fraud |   |
|  | Policies   |           | Location   |           | Session|  | Graph |   |
|  | Claims     |           | History    |           | Rate   |  | Rings |   |
|  | Payouts    |           |            |           | Limits |  |       |   |
|  +------------+           +------------+           +--------+  +-------+   |
|                                                                             |
|  +----------------------------------------------------------------------+  |
|  |                    MESSAGE QUEUE (Apache Kafka)                        |  |
|  |  Topics: telemetry_stream | claim_events | fraud_alerts | payouts    |  |
|  +----------------------------------------------------------------------+  |
|                                     |                                       |
|                                     v                                       |
|  +----------------------------------------------------------------------+  |
|  |                    ML SERVICES (Python FastAPI)                        |  |
|  |  +--------------+ +--------------+ +--------------+ +--------------+ |  |
|  |  |   Premium    | |    Fraud     | |     Ring     | |   Anomaly    | |  |
|  |  |  Calculator  | |   Detector   | |   Detector   | |  Detection   | |  |
|  |  |  (XGBoost)   | |  (Ensemble)  | |   (Neo4j)    | |  (Isolation) | |  |
|  |  +--------------+ +--------------+ +--------------+ +--------------+ |  |
|  +----------------------------------------------------------------------+  |
|                                                                             |
|  +----------------------------------------------------------------------+  |
|  |                    EXTERNAL INTEGRATIONS                              |  |
|  |  Weather API (IMD/OpenWeather) | Zomato/Swiggy OAuth | Razorpay     |  |
|  +----------------------------------------------------------------------+  |
|                                                                             |
+-----------------------------------------------------------------------------+
```

### Technology Stack

| Layer | Technology | Purpose |
|:---|:---|:---|
| Mobile | Kotlin, MVVM, Room, WorkManager | Android app with offline-first telemetry |
| Frontend | React 18, TypeScript, MUI, Mapbox | Admin dashboard with real-time monitoring |
| Backend APIs | Node.js (Express) | REST APIs, authentication, business logic |
| ML Services | Python (FastAPI) | Fraud detection, premium calculation |
| Transactional DB | PostgreSQL | Users, policies, claims, payouts |
| Time-Series DB | TimescaleDB | Telemetry data, location history |
| Cache | Redis | Session storage, rate limiting, real-time scoring |
| Graph DB | Neo4j | Fraud ring detection, social graphs |
| Streaming | Apache Kafka | Async claim processing, telemetry ingestion |
| ML Frameworks | scikit-learn, XGBoost, TensorFlow | Model training and inference |
| DevOps | Docker, Kubernetes, GitHub Actions | Containerization, orchestration, CI/CD |
| Cloud | AWS (EC2, RDS, S3, EKS) | Production hosting |

---

## Development Roadmap — Phase 1: Foundation (Weeks 1–2)

| Week | Focus | Deliverables |
|:---:|:---|:---|
| 1 | Research and Architecture | Persona definition, Tech stack selection, Fraud strategy |
| 2 | MVP Planning | API design, Database schema, ML model prototyping |

---

## Risk Assessment and Mitigation

| Risk | Impact | Probability | Mitigation Strategy |
|:---|:---:|:---:|:---|
| Sophisticated spoofing bypassing detection layers | High | Medium | Continuous model retraining, adversarial ML research, human review fallback |
| False positives blocking honest workers | Medium | Low | Whitelist program, false positive compensation, 24/7 support |
| Weather API downtime | Medium | Medium | Multiple API providers (IMD + OpenWeather + AccuWeather) with fallback |
| Device compatibility issues | Medium | Medium | Support Android 8+ only, graceful degradation for missing sensors |
| Regulatory compliance | High | Low | IRDAI sandbox application, transparent pricing, clear terms |
| Liquidity drain from mass claims | High | Medium | Circuit breaker logic, reinsurance partnership, reserve fund |

---

## Success Metrics

### Technical KPIs

| Metric | Target | Measurement |
|:---|:---:|:---|
| Fraud detection rate | >95% | Flagged fraud / actual fraud (post-review) |
| False positive rate | <2% | Honest claims flagged / total honest claims |
| Claim processing time | <30 seconds | Time from trigger to payout |
| Telemetry coverage | >90% | Devices sending complete sensor data |
| ML model accuracy | >90% | Correct fraud classification |
| System uptime | 99.9% | Availability during peak hours |

### Business KPIs

| Metric | Target | Measurement |
|:---|:---:|:---|
| User acquisition | 5,000 by Phase 3 | Registered delivery partners |
| Premium collection | Rs. 2,00,000/week | Weekly premium revenue |
| Loss ratio | 60–70% | Payouts / Premiums |
| User retention | >80% week-over-week | Active policies / total registered |
| NPS | >40 | Post-payout survey |

### Fraud Prevention Impact

| Metric | Target |
|:---|:---:|
| Fraudulent claims prevented | 500+ per week |
| Liquidity saved | Rs. 2,50,000+ per week |
| Fraud ring detection time | <15 minutes |
| Honest worker satisfaction | 95% positive feedback |

---

## Conclusion

GigSaathi addresses a critical market gap with a technically deep, fraud-resistant architecture. The multi-layer defense — sensor fusion, behavioral analytics, and graph-based ring detection — makes large-scale spoofing attacks economically unviable.

### Differentiators

| # | Differentiator | Impact |
|:---:|:---|:---|
| 1 | Physics-Based Validation | We verify reality, not just GPS coordinates |
| 2 | Graduated UX | Honest workers face zero friction; fraudsters face impossible barriers |
| 3 | Real-Time Detection | Fraud rings identified within 15 minutes, before mass payouts |
| 4 | Scalable Architecture | Kafka + TimescaleDB + Neo4j handles millions of daily events |
| 5 | Weekly Pricing | Aligns with gig workers' cash flow, drives adoption |

## Appendix

### A. API Endpoints

| Endpoint | Method | Purpose |
|:---|:---:|:---|
| `/api/v1/auth/register` | `POST` | User registration with phone OTP |
| `/api/v1/auth/verify-platform` | `POST` | Zomato/Swiggy credential verification |
| `/api/v1/policy/quote` | `GET` | Get dynamic weekly premium |
| `/api/v1/policy/purchase` | `POST` | Purchase weekly policy |
| `/api/v1/claim/submit` | `POST` | Submit claim with telemetry |
| `/api/v1/telemetry/batch` | `POST` | Upload batched sensor data |
| `/api/v1/user/whitelist` | `POST` | Admin: add to whitelist |

### B. Database Schema

```sql
-- Users table
CREATE TABLE users (
    id              UUID PRIMARY KEY,
    phone           VARCHAR(15) UNIQUE,
    aadhaar_hash    VARCHAR(255),
    platform_type   VARCHAR(20),
    platform_id     VARCHAR(50),
    trust_score     FLOAT DEFAULT 0.5,
    created_at      TIMESTAMP
);

-- Policies table
CREATE TABLE policies (
    id              UUID PRIMARY KEY,
    user_id         UUID REFERENCES users(id),
    weekly_premium  DECIMAL(10,2),
    coverage_amount DECIMAL(10,2),
    start_date      DATE,
    end_date        DATE,
    status          VARCHAR(20)
);

-- Claims table
CREATE TABLE claims (
    id              UUID PRIMARY KEY,
    user_id         UUID REFERENCES users(id),
    policy_id       UUID REFERENCES policies(id),
    trigger_type    VARCHAR(50),
    location_lat    DECIMAL(10,8),
    location_lng    DECIMAL(11,8),
    fraud_score     FLOAT,
    status          VARCHAR(20),
    payout_amount   DECIMAL(10,2),
    created_at      TIMESTAMP
);

-- Telemetry table (TimescaleDB hypertable)
CREATE TABLE telemetry (
    time              TIMESTAMPTZ NOT NULL,
    user_id           UUID NOT NULL,
    claim_id          UUID,
    lat               DECIMAL(10,8),
    lng               DECIMAL(11,8),
    wifi_ssid         VARCHAR(255),
    wifi_bssid        VARCHAR(255),
    pressure_hpa      FLOAT,
    motion_stationary BOOLEAN,
    battery_level     INT,
    device_id         VARCHAR(255)
);
SELECT create_hypertable('telemetry', 'time');
```

### C. References

- [Guidewire DEVTrails 2026 Rulebook](https://github.com)
- [DEVTrails 2026 Usecase Document](https://github.com)
- [Android Sensors API Documentation](https://developer.android.com/guide/topics/sensors)
- [Google SafetyNet Attestation](https://developer.android.com/training/safetynet)
- [TimescaleDB for Time-Series Data](https://www.timescale.com/)

---

<div align="center">


**Team:** Team Console | **Phase:** 1 — Ideation & Foundation | 
</div>