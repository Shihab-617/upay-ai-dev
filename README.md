# UPAY SENTINEL AI — TrustGraph Financial Intelligence Platform
> **DIU CPC × upay — AI Hackathon 2026 | AI DEV FEST 2026**  
> **Official Track:** Trust & Risk Intelligence  
> **Live Production URL:** [https://upa-ai-dev.netlify.app/](https://upa-ai-dev.netlify.app/)  
> **Repository:** [https://github.com/Shihab-617/upay-ai-dev](https://github.com/Shihab-617/upay-ai-dev)  

[![Live Demo](https://img.shields.io/badge/Live_Deployment-upa--ai--dev.netlify.app-blue.svg?style=flat&logo=netlify)](https://upa-ai-dev.netlify.app/)
[![License: MIT](https://img.shields.io/badge/License-MIT-emerald.svg)](LICENSE)
[![Runtime](https://img.shields.io/badge/Node.js-%3E%3D18.0.0-green.svg?logo=node.js)](https://nodejs.org)
[![Vite](https://img.shields.io/badge/Vite-8.3-646CFF.svg?logo=vite)](https://vitejs.dev)
[![React](https://img.shields.io/badge/React-19.0-61DAFB.svg?logo=react)](https://react.dev)
[![AI Engine](https://img.shields.io/badge/Google_Gemini-3.8_Flash-8E75B2.svg?logo=google-gemini)](https://ai.google.dev)
[![Security Status](https://img.shields.io/badge/Security_Tests-35%2F35_PASS-success.svg)](scripts/verify-security.mjs)

---

## 1. Project Overview

### 1.1 The Problem Addressed
Mobile Financial Services (MFS) platforms like **upay** facilitate millions of high-frequency micro-transactions, P2P transfers, merchant checkouts, utility payments, and agent cash-outs daily. Traditional fraud detection systems rely predominantly on static, single-transaction threshold rules. In dynamic real-world environments, this approach creates two structural vulnerabilities:
1. **High False-Positive Fatigue:** Legitimate transactions—such as seasonal festival remittances, emergency medical expenses, or family transfers—trigger rigid threshold blocks, degrading customer trust and overwhelming manual compliance desks.
2. **Coordinated Syndicate Evasion:** Sophisticated criminal networks stay beneath static single-transaction thresholds by breaking stolen funds into small amounts (smurfing), using emulator farms, Account Takeover (ATO) techniques, and rapid multi-hop dispersion chains terminating at compromised cash-out agent hubs.

Single transactions rarely convey full risk context. Genuine financial threat is a combination of hardware novelty, velocity deviation, abnormal timing, non-habitual counterparties, and topological graph proximity to illicit cash-out clusters.

### 1.2 Proposed Solution & Purpose
**UPAY SENTINEL AI** is an explainable financial safety and risk intelligence platform engineered specifically for modern MFS ecosystems. The platform synthesizes deterministic transaction anomaly scoring, customer behavioral DNA profiling, topological graph intelligence (TrustGraph), and grounded Generative AI into a unified analyst workbench and customer protection system.

```
                    SYNTHETIC TRANSACTION INGESTION
                                  │
                                  ▼
                      FEATURE EXTRACTION ENGINE
                                  │
             ┌────────────────────┼────────────────────┐
             ▼                    ▼                    ▼
      TRANSACTION ENGINE   BEHAVIORAL ENGINE     GRAPH ENGINE
      (Velocity/Z-Score)   (Customer DNA/Time)  (TrustGraph ML)
             │                    │                    │
             └────────────────────┼────────────────────┘
                                  ▼
                     DETERMINISTIC RISK ENGINE
                    (Additive Signals: 0 - 100)
                                  │
                                  ▼
                         STRUCTURED EVIDENCE
                     (<evidence> Bounded Schema)
                                  │
                                  ▼
                      GROUNDED GEMINI COPILOT
                  (Explanatory AI Investigator)
```

---

## 2. Features & AI Implementation

| Feature Module | Implementation Details & AI Usage | Route |
| :--- | :--- | :--- |
| **Command Center Dashboard** | Real-time monitoring metrics (1,120 transactions, risk distributions, value-at-risk, top 5 anomaly signals, and high-risk case queue). | `#/dashboard` |
| **Topological TrustGraph** | Interactive force-directed network graph detecting multi-hop mule accounts, emulator sharing rings (`CLUSTER-SMURF-904`), and agent aggregation hubs (`AGENT-DEMO-007`). | `#/trustgraph` |
| **Grounded Gemini AI Copilot** | Conversational investigation assistant powered by **Google Gemini 3.8 Flash** with system telemetry grounding, IoC extraction, and SAR drafting. Dual-mode execution (Express backend + client-side static fallback). | `#/copilot` |
| **Transaction Directory** | Complete ledger with multi-attribute filtering (Status, Risk Level, Type), risk badges, and detailed transaction inspection views. | `#/transactions` |
| **Investigation Dossier** | Comprehensive forensic dossier with chronological attack timeline, audit trails, evidence cards, and 1-click mitigation actions. | `#/investigations` |
| **Customer Safety Shield** | Interactive customer-facing warning and verification flow with 15-minute soft quarantine escrow hold and self-service emergency fund freeze. | `#/safety/TX-DEMO-49281` |
| **Dynamic Rules Engine & Backtest** | Real-time rule authoring console with shadow mode execution and instantaneous historical backtesting across past transactions with false-positive rate estimation. | `#/admin` |
| **Four-Eyes Dual Authorization** | Cryptographic separation of duties requiring supervisor dual sign-off on critical freezes, preventing insider collusion. | `#/investigations` |
| **Cryptographic SHA-256 Audit Chain** | Immutable, tamper-evident Merkle-linked audit log trail with genesis block hash verification to satisfy regulatory non-repudiation. | `#/reports` |
| **Bangladesh Bank goAML XML Export** | One-click regulatory Suspicious Transaction Report (STR) compliant with FIU-standard schema for automated submission. | `#/reports` |
| **Responsible AI Governance** | Model explainability dashboard verifying demographic invariance, signal weight calibration, and zero reliance on protected attributes. | `#/responsible-ai` |
| **Simulation Lab** | Interactive scenario simulator allowing analysts to stress-test smurf waves, rapid drain bursts, and off-hours credential attacks. | `#/simulation` |

---

## 3. Technology Stack

- **Frontend:** React 19, TypeScript, Vite 8.3, Tailwind CSS v4, Lucide React, Recharts, Motion
- **Backend & APIs:** Node.js (>= 18), Express 4.21, TypeScript via `tsx`
- **Artificial Intelligence Models:**
  - **Google Gemini 3.8 Flash** (`gemini-3.8-flash`) — Primary analytical reasoning and case explanation
  - **Google Gemini 3.1 Flash Lite** (`gemini-3.1-flash-lite`) — Low-latency real-time inference
  - **Google Gemini 3.5 Flash Lite** (`gemini-3.5-flash-lite`) — High-efficiency conversational processing
  - **SDK:** `@google/genai` (v2.4.0) with direct client-side fallback service
- **Security & Data:** Cryptographic SHA-256 Merkle chain, Helmet security headers, Role-Based Access Control (RBAC), and 100% synthetic privacy-preserving dataset.

---

## 4. Requirements & Prerequisites

- **Runtime:** Node.js `>= 18.0.0` (LTS recommended, e.g., Node 20 or 22)
- **Package Manager:** `npm` `>= 9.0.0` (or `bun` / `pnpm`)
- **Memory & Hardware:** Any standard modern workstation (2GB+ RAM free)
- **Browser:** Any modern Chromium-based browser (Chrome, Edge, Brave), Firefox, or Safari

---

## 5. Installation and Setup

Step-by-step instructions to configure and run the project locally:

### Step 1: Clone the Repository
```bash
git clone https://github.com/Shihab-617/upay-ai-dev.git
cd upay-ai-dev
```

### Step 2: Install Dependencies
```bash
npm install
```

### Step 3: Configure Environment Variables
Copy the template configuration file:
```bash
cp .env.example .env
```
Open `.env` and set your Google Gemini API key:
```env
GEMINI_API_KEY="your_gemini_api_key_here"
```

---

## 6. Environment Variables

Create a `.env` file in the project root based on `.env.example`:

| Variable Name | Required | Default / Placeholder | Purpose |
| :--- | :--- | :--- | :--- |
| `GEMINI_API_KEY` | Optional* | `"YOUR_GEMINI_API_KEY"` | Google Gemini API key for live Copilot investigations (*built-in demo fallback included). |
| `VITE_GEMINI_API_KEY` | Optional* | `"YOUR_GEMINI_API_KEY"` | Frontend-accessible Gemini API key for direct client-side inference on static hosts. |
| `PORT` | Optional | `3000` | Port for the full-stack Express server. |
| `NODE_ENV` | Optional | `"development"` | Node runtime environment (`development` or `production`). |
| `APP_URL` | Optional | `"http://localhost:3000"` | Canonical base URL for the application. |
| `ADMIN_1_NAME` | Optional | `"Fahad Ahmed (Super Admin)"` | Pre-seeded Super Admin user display name. |
| `ADMIN_1_EMAIL` | Optional | `"diudevcis"` | Pre-seeded Super Admin login identifier. |
| `ADMIN_1_PASSWORD` | Optional | `"diudevcis"` | Pre-seeded Super Admin authentication secret. |

> *Note: For immediate evaluation without API key configuration, the platform includes a resilient client-side heuristic engine that provides fully structured, grounded analysis even offline.*

---

## 7. Run and Build Commands

| Command | Action | Output / Target |
| :--- | :--- | :--- |
| `npm run dev` | Starts full-stack development server with Vite middleware | `http://localhost:3000` |
| `npm run build` | Compiles optimized client-side SPA production bundle | `dist/` |
| `npm run start` | Boots production Express server serving compiled static assets | `http://0.0.0.0:3000` |
| `npm run preview` | Previews the compiled Vite production bundle locally | `http://localhost:4173` |
| `npm run lint` | Runs TypeScript static type checker across the codebase | Type analysis |

---

## 8. Live Deployment URL

### 🌟 Primary Production Deployment:
👉 **[https://upa-ai-dev.netlify.app/](https://upa-ai-dev.netlify.app/)**

### 🔑 Evaluation Access Credentials:
- **1-Click Super Admin Access:** Click the **`🚀 1-Click Enter as Super Admin (diudevcis)`** button on the sign-in page.
- **Manual Credentials:**
  - **Username / Identifier:** `diudevcis`
  - **Password:** `diudevcis`
- **Alternative Analyst Account:**
  - **Email:** `admin.nusrat@upay.demo`
  - **Password:** `diudevcis`

---

## 9. Testing & Verification Instructions

The repository includes comprehensive automated test suites to verify system integrity, access controls, race condition boundaries, and core analytical innovations:

### 1. Run Complete Security Verification Suite
Tests public routes, unauthenticated blocking, secure headers, credential validation, RBAC boundaries, and emergency lockdown controls:
```bash
npm run test:security
```
*Expected Result:* `35/35 PASSED`

### 2. Run Concurrent Race-Condition Test
Verifies atomic account ceiling limits under rapid parallel request bursts:
```bash
npm run test:race
```
*Expected Result:* `SUCCESS: Active accounts strictly bounded to <= 5.`

### 3. Run 5-Innovation Feature Validation Suite
Executes end-to-end programmatic tests for soft quarantine escrow, dynamic rule shadow backtests, token FinOps, dual authorization, cryptographic Merkle audit verification, and BFIU goAML XML export:
```bash
npm run test:innovations
```
*Expected Result:* `ALL 5 INNOVATIONS FULLY OPERATIONAL & VERIFIED!`

---

## 10. Additional Configuration & Deployment Notes

- **Static Deployment Compatibility:** The client includes [`geminiClientService.ts`](src/services/geminiClientService.ts) and [`api.ts`](src/services/api.ts) resilient fallbacks. When hosted statically on platforms like Netlify, client-side routing is handled through [`_redirects`](public/_redirects) (`/* /index.html 200`) and hash deep-linking (`#/dashboard`, `#/trustgraph`, `#/investigations`).
- **Data Privacy & Compliance:** The application operates on 100% synthetic, mathematically modeled MFS transaction telemetry. No personally identifiable information (PII) or real customer banking records are stored or transmitted.

---

## 👥 Hackathon Team Members

- **Md. Fahad (`@fahad3235`)** — Lead System Developer
- **Md. Muhsinul Islam (`@muhsinulmuin`)** — Product Manager, Technical Documentation & Pitch Lead
- **Shihab Sarker (`@Shihab-617`)** — AI Product Strategist (DIU Student ID: `262-16-050`)
