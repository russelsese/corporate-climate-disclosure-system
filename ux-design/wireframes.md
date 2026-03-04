# CCDS — Wireframes (ASCII)

All wireframes are desktop-first at 1280px unless noted as mobile. Dimensions are illustrative. `[ ]` = button/input, `│ ─` = layout borders, `▓` = filled/active state.

---

## WF-01: Login Screen

```
┌──────────────────────────────────────────────────────────────┐
│                                                              │
│                    [CCDS Logo + Wordmark]                    │
│              Corporate Climate Disclosure System             │
│                                                              │
│         ┌────────────────────────────────────────┐          │
│         │                                        │          │
│         │  Work email                            │          │
│         │  ┌──────────────────────────────────┐  │          │
│         │  │ name@company.com.au              │  │          │
│         │  └──────────────────────────────────┘  │          │
│         │                                        │          │
│         │  Password                              │          │
│         │  ┌──────────────────────────────────┐  │          │
│         │  │ ••••••••••                  [👁] │  │          │
│         │  └──────────────────────────────────┘  │          │
│         │                                        │          │
│         │  [       Sign in securely        ]     │          │
│         │                                        │          │
│         │  Forgot password?   |   Need access?   │          │
│         └────────────────────────────────────────┘          │
│                                                              │
│         🔒  Secured by MFA  ·  Data hosted in Australia     │
│                                                              │
└──────────────────────────────────────────────────────────────┘
```

---

## WF-02: Eligibility Check (Public Tool — no login)

```
┌──────────────────────────────────────────────────────────────────────┐
│  [CCDS Logo]            Eligibility Check                            │
├──────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  Check if your company must report under AASB S2                     │
│  ─────────────────────────────────────────────────────────           │
│                                                                      │
│  Answer about your consolidated group (parent + all subsidiaries)   │
│                                                                      │
│  ┌────────────────────────────────────────────────────────────┐     │
│  │  1. Consolidated revenue (AUD)                             │     │
│  │     ○ Under $50 million                                    │     │
│  │     ○ $50M – $199M                                         │     │
│  │     ○ $200M – $499M                                        │     │
│  │     ○ $500M or more                                        │     │
│  ├────────────────────────────────────────────────────────────┤     │
│  │  2. Consolidated gross assets (AUD)                        │     │
│  │     ○ Under $25 million                                    │     │
│  │     ○ $25M – $499M                                         │     │
│  │     ○ $500M – $999M                                        │     │
│  │     ○ $1 billion or more                                   │     │
│  ├────────────────────────────────────────────────────────────┤     │
│  │  3. Number of employees                                    │     │
│  │     ○ Fewer than 50                                        │     │
│  │     ○ 50 – 99                                              │     │
│  │     ○ 100 – 499                                            │     │
│  │     ○ 500 or more                                          │     │
│  ├────────────────────────────────────────────────────────────┤     │
│  │  4. Are you an NGER controlling corporation?               │     │
│  │     ○ Yes    ○ No    ○ Not sure                            │     │
│  └────────────────────────────────────────────────────────────┘     │
│                                                                      │
│  [   Check my eligibility   ]                                        │
│                                                                      │
│  ─────────── RESULT ───────────                                      │
│  ┌────────────────────────────────────────────────────────────┐     │
│  │  ✅  You are a GROUP 2 reporting entity                    │     │
│  │                                                            │     │
│  │  First mandatory reporting period:                         │     │
│  │  Financial year beginning on or after 1 July 2026         │     │
│  │                                                            │     │
│  │  You must prepare a Sustainability Report under            │     │
│  │  AASB S2 for that period.                                  │     │
│  │                                                            │     │
│  │  [  Set up your CCDS account  ]   [ Save result as PDF ]   │     │
│  └────────────────────────────────────────────────────────────┘     │
└──────────────────────────────────────────────────────────────────────┘
```

---

## WF-03: Main Dashboard (ESG Manager view)

```
┌──────────────────────────────────────────────────────────────────────────────────────┐
│  [≡] CCDS                           FY2026 Reporting Period        [🔔 3] [SM avatar] │
├──────────────┬─────────────────────────────────────────────────────────────────────  │
│              │                                                                        │
│  Dashboard   │  Good morning, Sarah.   Deadline: 30 Sep 2026  ██████░░░░  62 days   │
│  ─────────   │  ─────────────────────────────────────────────────────────────────    │
│  Setup       │                                                                        │
│  Governance  │  ┌──────────────────┐ ┌──────────────────┐ ┌──────────────────┐      │
│  Strategy    │  │ GOVERNANCE       │ │ STRATEGY         │ │ RISK MANAGEMENT  │      │
│  Risk Mgmt   │  │ ▓▓▓▓▓▓▓░░░  75% │ │ ▓▓▓▓░░░░░░  40% │ │ ▓▓░░░░░░░░  20% │      │
│  Emissions   │  │                  │ │                  │ │                  │      │
│  Metrics     │  │ ✅ Board entered │ │ ✅ Risks entered │ │ ✅ Register up  │      │
│  ─────────   │  │ ⚠️ Pending CFO  │ │ ⏳ CTP in draft  │ │ ❌ Process docs │      │
│  Reports     │  │    approval      │ │ ❌ Scenario 2°C  │ │    not done      │      │
│  Evidence    │  │                  │ │    not started   │ │                  │      │
│  Audit Log   │  └──────────────────┘ └──────────────────┘ └──────────────────┘      │
│  ─────────   │                                                                        │
│  Notifs 🔴3 │  ┌──────────────────────────────────────────────────────────────────┐ │
│  Admin       │  │ EMISSIONS & ENERGY + METRICS & TARGETS                           │ │
│              │  │                                                                  │ │
│              │  │ Emissions:  ▓▓▓▓▓▓▓░░░  70%    Metrics: ▓▓░░░░░░░░  25%        │ │
│              │  │                                                                  │ │
│              │  │  Sites submitted: 5 / 8         Targets defined: 3 / 5         │ │
│              │  │  ⚠️ 3 sites overdue             ❌ Actuals not updated          │ │
│              │  └──────────────────────────────────────────────────────────────────┘ │
│              │                                                                        │
│              │  MY TASKS  ───────────────────────────────────────────────────         │
│              │  ┌──────────────────────────────────────────────────────────────────┐ │
│              │  │ ⚠️  Dandenong Plant — emissions data overdue (due 3 days ago)   │ │
│              │  │     [Send reminder]  [View site]                                 │ │
│              │  ├──────────────────────────────────────────────────────────────────┤ │
│              │  │ 📝  Strategy section — 2°C scenario analysis not started        │ │
│              │  │     [Go to Strategy]                                             │ │
│              │  ├──────────────────────────────────────────────────────────────────┤ │
│              │  │ ✅  CFO approved Governance section — no action needed           │ │
│              │  └──────────────────────────────────────────────────────────────────┘ │
│              │                                                                        │
└──────────────┴────────────────────────────────────────────────────────────────────────┘
```

---

## WF-04: Dashboard (Executive / CFO View)

```
┌──────────────────────────────────────────────────────────────────────────────────────┐
│  [≡] CCDS                                FY2026 · Executive View    [🔔 1] [AC] │
├──────────────┬─────────────────────────────────────────────────────────────────────  │
│  Dashboard   │                                                                        │
│  Reports     │  FY2026 Compliance Status                      Deadline: 30 Sep 2026   │
│  Admin       │  ─────────────────────────────────────────────────────────────────     │
│              │                                                                        │
│              │  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐              │
│              │  │GOVERNANCE│  │STRATEGY  │  │   RISK   │  │EMISSIONS │              │
│              │  │          │  │          │  │   MGMT   │  │& METRICS │              │
│              │  │  ✅ CFO  │  │ ⏳ DRAFT │  │ ⏳ DRAFT │  │ ⚠️ DATA  │              │
│              │  │ APPROVED │  │          │  │          │  │ PENDING  │              │
│              │  │          │  │ Ready    │  │          │  │          │              │
│              │  │ [Review] │  │ soon     │  │ [Review] │  │          │              │
│              │  └──────────┘  └──────────┘  └──────────┘  └──────────┘              │
│              │                                                                        │
│              │  ITEMS AWAITING YOUR APPROVAL  ────────────────────────────           │
│              │  ┌──────────────────────────────────────────────────────────────────┐ │
│              │  │  Governance Disclosure — submitted 14 Feb 2026                   │ │
│              │  │  Prepared by: Sarah Mitchell                                     │ │
│              │  │  [Preview disclosure]                     [Approve]  [Request ↩] │ │
│              │  └──────────────────────────────────────────────────────────────────┘ │
│              │                                                                        │
│              │  TOTAL GHG EMISSIONS (year to date)  ─────────────────────────        │
│              │  Scope 1:  1,240 tCO₂e   │  Scope 2 (loc): 3,890 tCO₂e              │
│              │  Scope 3:  ——— (Year 1)  │  Total: 5,130 tCO₂e                      │
│              │                                                                        │
│              │  [Download Executive Summary PDF]     [View Full Report Draft]        │
│              │                                                                        │
└──────────────┴────────────────────────────────────────────────────────────────────────┘
```

---

## WF-05: Site Emissions Entry (Mobile — Site Manager)

```
  ┌───────────────────────────┐
  │ ← Back    CCDS         🔔 │
  │ ───────────────────────── │
  │ Dandenong Plant           │
  │ Q4 2025 · Due 15 Feb 2026 │
  │ ███████░░░  65% complete  │
  │ ───────────────────────── │
  │                           │
  │ ▼ SCOPE 1 — Direct        │
  │ ┌─────────────────────┐   │
  │ │ Natural gas         │   │
  │ │ Volume consumed     │   │
  │ │ ┌─────────────────┐ │   │
  │ │ │ 4,800       GJ ▼│ │   │
  │ │ └─────────────────┘ │   │
  │ │ ℹ️ From gas meter   │   │
  │ │    or utility bill  │   │
  │ │                     │   │
  │ │ = 247 tCO₂e  ✓     │   │
  │ └─────────────────────┘   │
  │                           │
  │ ┌─────────────────────┐   │
  │ │ Diesel (site use)   │   │
  │ │ ┌─────────────────┐ │   │
  │ │ │ 28,000      L  ▼│ │   │
  │ │ └─────────────────┘ │   │
  │ │ = 75 tCO₂e  ✓      │   │
  │ └─────────────────────┘   │
  │                           │
  │ ▼ SCOPE 2 — Electricity   │
  │ ┌─────────────────────┐   │
  │ │ Electricity used    │   │
  │ │ ┌─────────────────┐ │   │
  │ │ │ 180,000    kWh ▼│ │   │
  │ │ └─────────────────┘ │   │
  │ │ 📎 Upload bill      │   │
  │ │ [utility-q4.pdf ✓]  │   │
  │ │ = 146 tCO₂e  ✓     │   │
  │ └─────────────────────┘   │
  │                           │
  │ ▼ SCOPE 3                 │
  │ ┌─────────────────────┐   │
  │ │ ℹ️ Optional — Year 1│   │
  │ │ [Skip for now]      │   │
  │ └─────────────────────┘   │
  │                           │
  │ ───────────────────────── │
  │ TOTAL THIS SITE           │
  │ Scope 1:   322 tCO₂e     │
  │ Scope 2:   146 tCO₂e     │
  │ ───────────────────────── │
  │                           │
  │ [  Save Draft  ]          │
  │ [  Submit Data ]          │
  │                           │
  └───────────────────────────┘
```

---

## WF-06: Risk Register

```
┌──────────────────────────────────────────────────────────────────────────────────────┐
│  [≡] CCDS  >  Risk Management  >  Climate Risk Register                              │
├──────────────┬─────────────────────────────────────────────────────────────────────  │
│  [nav]       │  Climate Risk Register                          [+ Add Risk]           │
│              │                                                                        │
│              │  Filter: [All Types ▼]  [All Time Horizons ▼]  [All Statuses ▼]       │
│              │                                                                        │
│              │  ┌─────┬──────────────────────┬───────────────┬───────────┬──────────┬─────────────────┐│
│              │  │ ID  │ Risk / Opportunity    │ Type          │ Horizon   │ Like.×   │ Status          ││
│              │  │     │                       │               │           │  Mag.    │                 ││
│              │  ├─────┼──────────────────────┼───────────────┼───────────┼──────────┼─────────────────┤│
│              │  │ R01 │ Carbon price increase │ Transition —  │ Short     │ H × H    │ ✅ Assessed     ││
│              │  │     │ on fuel & energy      │ Policy/Legal  │ (1–3 yr)  │ 🔴 HIGH  │                 ││
│              │  ├─────┼──────────────────────┼───────────────┼───────────┼──────────┼─────────────────┤│
│              │  │ R02 │ Flood damage to       │ Physical —    │ Long      │ M × H    │ ✅ Assessed     ││
│              │  │     │ Dandenong facility    │ Acute         │ (>10 yr)  │ 🟠 MED   │                 ││
│              │  ├─────┼──────────────────────┼───────────────┼───────────┼──────────┼─────────────────┤│
│              │  │ R03 │ Customer shift to     │ Transition —  │ Medium    │ M × M    │ ⏳ In progress  ││
│              │  │     │ low-carbon suppliers  │ Market        │ (3–10 yr) │ 🟡 LOW   │                 ││
│              │  ├─────┼──────────────────────┼───────────────┼───────────┼──────────┼─────────────────┤│
│              │  │ O01 │ Renewable energy       │ Opportunity  │ Short     │ H × M    │ ✅ Assessed     ││
│              │  │     │ cost savings          │ Resource eff. │ (1–3 yr)  │ 🟢 OPP   │                 ││
│              │  └─────┴──────────────────────┴───────────────┴───────────┴──────────┴─────────────────┘│
│              │                                                                        │
│              │  Showing 4 of 12 entries   [< Prev]  Page 1 of 3  [Next >]            │
│              │                                                                        │
│              │  [Export Register as CSV]                                              │
│              │                                                                        │
│              │  ─── RISK DETAIL (click row to expand) ───────────────────────────    │
│              │  ┌──────────────────────────────────────────────────────────────────┐ │
│              │  │ R01 — Carbon price increase on fuel & energy                     │ │
│              │  │ AASB S2 ref: §23(a), §24                                         │ │
│              │  │ Financial effect: Revenue impact -$2.4M p.a. (estimated)         │ │
│              │  │ Controls: Energy efficiency programme, renewable PPA in progress  │ │
│              │  │ [Edit]  [Link evidence]  [View in Disclosure]                     │ │
│              │  └──────────────────────────────────────────────────────────────────┘ │
└──────────────┴────────────────────────────────────────────────────────────────────────┘
```

---

## WF-07: Approval Workflow Screen (CFO reviewing a section)

```
┌──────────────────────────────────────────────────────────────────────────────────────┐
│  [≡] CCDS  >  Governance  >  Disclosure  >  Review & Approval                        │
├──────────────┬─────────────────────────────────────────────────────────────────────  │
│  [nav]       │                                                                        │
│              │  Governance Disclosure — FY2026                                        │
│              │  ┌──────────────────────────────────────────────────────────────────┐ │
│              │  │ APPROVAL CHAIN                                                   │ │
│              │  │  [1. Prepared by Sarah Mitchell ✓]                               │ │
│              │  │       ↓                                                           │ │
│              │  │  [2. CFO Review — YOU ARE HERE  ⏳]                              │ │
│              │  │       ↓                                                           │ │
│              │  │  [3. Board Director Approval — pending]                           │ │
│              │  └──────────────────────────────────────────────────────────────────┘ │
│              │                                                                        │
│              │  ┌──────────────────────────────────┐  ┌─────────────────────────┐   │
│              │  │  DISCLOSURE NARRATIVE             │  │  AASB S2 REFERENCE      │   │
│              │  │  ─────────────────────────────── │  │  ─────────────────────  │   │
│              │  │  Board oversight of climate-      │  │  §6 — Governance        │   │
│              │  │  related risks                    │  │  §7(a) Board oversight  │   │
│              │  │                                   │  │  §7(b) Management role  │   │
│              │  │  The Board's Audit & Risk         │  │  §8 Remuneration        │   │
│              │  │  Committee (BARC) has             │  │  §9 Transition plan     │   │
│              │  │  oversight responsibility for     │  │                         │   │
│              │  │  climate-related risks. BARC      │  │  ✅ All mandatory refs  │   │
│              │  │  meets quarterly and reviews      │  │     covered             │   │
│              │  │  the climate risk register at     │  │                         │   │
│              │  │  each meeting...                  │  │  PRIOR YEAR COMPARISON  │   │
│              │  │                                   │  │  [Toggle ON/OFF]        │   │
│              │  │  [See full narrative →]           │  │                         │   │
│              │  └──────────────────────────────────┘  └─────────────────────────┘   │
│              │                                                                        │
│              │  SUPPORTING EVIDENCE (3 documents)                                    │
│              │  ├── BARC_Charter_v3.pdf            [Preview] [Download]             │
│              │  ├── BoardMinutes_Q3_2025.pdf        [Preview] [Download]             │
│              │  └── ClimatePolicy_2025.pdf          [Preview] [Download]             │
│              │                                                                        │
│              │  ─────────────────────────────────────────────────────────────────    │
│              │  YOUR DECISION                                                         │
│              │                                                                        │
│              │  Optional comment:                                                     │
│              │  ┌──────────────────────────────────────────────────────────────────┐ │
│              │  │                                                                  │ │
│              │  └──────────────────────────────────────────────────────────────────┘ │
│              │                                                                        │
│              │  [  ✅ Approve Section  ]      [  ↩ Request Changes  ]                │
│              │                                                                        │
└──────────────┴────────────────────────────────────────────────────────────────────────┘
```

---

## WF-08: Report Builder

```
┌──────────────────────────────────────────────────────────────────────────────────────┐
│  [≡] CCDS  >  Reports  >  Sustainability Report Builder                              │
├──────────────┬─────────────────────────────────────────────────────────────────────  │
│  [nav]       │                                                                        │
│              │  Generate Sustainability Report — FY2026                               │
│              │                                                                        │
│              │  SECTION READINESS  ────────────────────────────────────────────────  │
│              │  ┌─────────────────────────────────────────────────────────────────┐  │
│              │  │  ✅ Governance          CFO Approved · Board Approved            │  │
│              │  │  ✅ Strategy            CFO Approved                             │  │
│              │  │  ✅ Risk Management     CFO Approved                             │  │
│              │  │  ✅ Emissions & Metrics CFO Approved                             │  │
│              │  │                                                                  │  │
│              │  │  All sections approved. Report is ready to generate.  ✅        │  │
│              │  └─────────────────────────────────────────────────────────────────┘  │
│              │                                                                        │
│              │  OPTIONS  ─────────────────────────────────────────────────────────   │
│              │  ☑ Include prior-year comparison                                      │
│              │  ☑ Show AASB S2 paragraph references (recommended for assurance)     │
│              │  ☐ Include liability protection notices on Scope 3 / CTP sections    │
│              │                                                                        │
│              │  [  Generate Preview  ]                                               │
│              │                                                                        │
│              │  ─── REPORT PREVIEW ──────────────────────────────────────────────   │
│              │  ┌──────────────────────────────────────┐  ┌──────────────────────┐  │
│              │  │  SUSTAINABILITY REPORT FY2026         │  │  AASB S2 INDEX       │  │
│              │  │  ─────────────────────────────────── │  │  ───────────────────  │  │
│              │  │  1. Governance ..................... 3│  │  §6 Governance .... 3 │  │
│              │  │     1.1 Board oversight               │  │  §10 Strategy ..... 8 │  │
│              │  │     1.2 Management responsibility     │  │  §23 Risk Mgmt ... 14 │  │
│              │  │     1.3 Remuneration                  │  │  §29 Metrics ..... 18 │  │
│              │  │  2. Strategy ................... 8    │  │                      │  │
│              │  │     2.1 Risks & opportunities         │  │  All mandatory       │  │
│              │  │     2.2 Scenario analysis             │  │  paragraphs: ✅      │  │
│              │  │     2.3 Transition plan               │  │  Optional disclosed: │  │
│              │  │  3. Risk Management ........... 14    │  │  8 of 12             │  │
│              │  │  4. Metrics & Targets ......... 18    │  │                      │  │
│              │  │  [Scroll to read full report]         │  │                      │  │
│              │  └──────────────────────────────────────┘  └──────────────────────┘  │
│              │                                                                        │
│              │  EXPORT  ──────────────────────────────────────────────────────────   │
│              │  [ 📄 Download PDF ]  [ 📝 Download DOCX ]  [ 📦 Assurance Pack ZIP ] │
│              │  [ 📋 Executive Summary PDF ]                                          │
│              │                                                                        │
│              │  [ 🔒 Finalise & Lock Report ]  ← locks version, triggers change-lock │
│              │                                                                        │
└──────────────┴────────────────────────────────────────────────────────────────────────┘
```

---

## WF-09: Audit Log Viewer (Auditor view)

```
┌──────────────────────────────────────────────────────────────────────────────────────┐
│  [≡] CCDS  >  Audit Log                        [Read Only — Auditor Access]          │
├──────────────┬─────────────────────────────────────────────────────────────────────  │
│  [nav]       │  Audit Log — FY2026                                                   │
│              │                                                                        │
│              │  Filter: [All Modules ▼]  [All Users ▼]  [Date: Jan–Mar 2026 ▼]      │
│              │  Search: [                                           🔍 ]              │
│              │                                                                        │
│              │  ┌──────────────────┬──────────────────┬────────────────┬───────────┐ │
│              │  │ Timestamp        │ User             │ Module / Field │ Change    │ │
│              │  ├──────────────────┼──────────────────┼────────────────┼───────────┤ │
│              │  │ 14 Feb 10:42 AM  │ Sarah Mitchell   │ Governance /   │ Updated   │ │
│              │  │                  │ (ESG Manager)    │ BARC oversight │ text [+]  │ │
│              │  ├──────────────────┼──────────────────┼────────────────┼───────────┤ │
│              │  │ 14 Feb 10:38 AM  │ David Park       │ Emissions /    │ Changed   │ │
│              │  │                  │ (Site Mgr)       │ Dandenong /    │ 4200 GJ → │ │
│              │  │                  │                  │ Gas volume     │ 4800 GJ   │ │
│              │  │                  │                  │                │ [Reason:  │ │
│              │  │                  │                  │                │ Meter read│ │
│              │  │                  │                  │                │ corrected]│ │
│              │  ├──────────────────┼──────────────────┼────────────────┼───────────┤ │
│              │  │ 13 Feb 4:15 PM   │ Alex Chen (CFO)  │ Governance /   │ Approved  │ │
│              │  │                  │                  │ Disclosure     │ section   │ │
│              │  └──────────────────┴──────────────────┴────────────────┴───────────┘ │
│              │                                                                        │
│              │  Showing 3 of 847 log entries   [< Prev]  1  2 ... 85  [Next >]       │
│              │                                                                        │
│              │  AUDIT QUERIES  ─────────────────────────────────────────────────     │
│              │  ┌──────────────────────────────────────────────────────────────────┐ │
│              │  │  [+ Raise New Query]                                             │ │
│              │  │                                                                  │ │
│              │  │  Q01 — Diesel consumption query (Open)                           │ │
│              │  │  "Dandenong diesel higher than prior year — please explain"       │ │
│              │  │  Raised: 20 Feb · Assigned to: Sarah Mitchell · [View thread]    │ │
│              │  └──────────────────────────────────────────────────────────────────┘ │
│              │                                                                        │
│              │  [Export full audit log as CSV]                                        │
│              │                                                                        │
└──────────────┴────────────────────────────────────────────────────────────────────────┘
```

---

## WF-10: Notifications Panel (slide-out)

```
         ┌──────────────────────────────────────┐
         │  Notifications           [Mark all ✓]│
         ├──────────────────────────────────────┤
         │ 🔴 OVERDUE                           │
         │ ─────────────────────────────────── │
         │ Dandenong Plant emissions data        │
         │ was due 3 days ago.                   │
         │ [Send reminder]   [View site]         │
         ├──────────────────────────────────────┤
         │ 🟡 ACTION NEEDED                     │
         │ ─────────────────────────────────── │
         │ Governance section is awaiting       │
         │ your approval.                        │
         │ [Review now]                          │
         ├──────────────────────────────────────┤
         │ ℹ️ INFO                              │
         │ ─────────────────────────────────── │
         │ Auditor Marcus Thompson has raised    │
         │ a query on Scope 1 emissions.         │
         │ [View query]                          │
         ├──────────────────────────────────────┤
         │ ✅ COMPLETED                         │
         │ ─────────────────────────────────── │
         │ Footscray Office submitted            │
         │ Q4 emissions data. ✓                 │
         └──────────────────────────────────────┘
```
