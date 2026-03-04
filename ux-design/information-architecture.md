# CCDS — Information Architecture

## Navigation Philosophy

The system presents a **role-filtered view** of the same underlying data. A site manager should never see the risk register; a board member should never see raw emission factor tables. Navigation adapts to the logged-in user's role without requiring separate portals.

---

## Role-Based Navigation Matrix

| Navigation Section | ESG Manager | CFO / Finance | Site Manager | Board Director | Auditor | Company Secretary |
|---|---|---|---|---|---|---|
| Dashboard | Full | Executive view | My Tasks only | Executive view | Audit overview | Compliance view |
| Setup & Eligibility | Full edit | Read | — | — | Read | Read |
| Governance | Full edit | Approve | — | Approve | Read | Read |
| Strategy & Transition | Full edit | Approve | — | Read | Read | Read |
| Risk Management | Full edit | Approve | — | Read | Read | Read |
| Emissions & Energy | Full edit | Read | Enter own site | — | Read | — |
| Metrics & Targets | Full edit | Read | — | Read | Read | Read |
| Reports | Generate/export | Download | — | Download (exec) | Download (audit) | Download (final) |
| Evidence Library | Full | Read | Upload | — | Read | Read |
| Audit Log | Read | — | — | — | Full read | Read |
| Administration | Full | User mgmt | — | — | — | — |

---

## Full Site Map

```
CCDS Application
│
├── PUBLIC (pre-login)
│   ├── Login
│   ├── Forgot Password / MFA Setup
│   └── Eligibility Check (public tool, no login required)
│
└── AUTHENTICATED
    │
    ├── 1. DASHBOARD
    │   ├── Executive Summary (Board, CFO view)
    │   ├── Reporting Progress (ESG, Legal view)
    │   ├── My Tasks (Site Manager view)
    │   └── Audit Overview (Auditor view)
    │
    ├── 2. SETUP & ELIGIBILITY
    │   ├── 2.1 Company Profile
    │   │   ├── Organisation details (name, ABN, ACN, sector, FY end)
    │   │   ├── Group structure (parent + subsidiaries)
    │   │   └── Reporting period configuration
    │   ├── 2.2 Eligibility Assessment (Wizard)
    │   │   ├── Step 1 — Financial thresholds
    │   │   ├── Step 2 — Employee count
    │   │   ├── Step 3 — NGER status
    │   │   └── Step 4 — Result: Group + first reporting date
    │   ├── 2.3 Sites & Facilities
    │   │   ├── Add / edit site
    │   │   ├── Assign site manager
    │   │   └── Site reporting periods
    │   └── 2.4 User Management
    │       ├── Invite users
    │       ├── Assign roles
    │       └── Manage access (read / edit / approve)
    │
    ├── 3. GOVERNANCE
    │   ├── 3.1 Board Oversight
    │   │   ├── Committee structure (name, charter, members)
    │   │   ├── Oversight activities log (meeting dates, agenda items)
    │   │   └── Evidence: board minutes, charters (upload)
    │   ├── 3.2 Management Responsibilities
    │   │   ├── Role register (title, climate responsibilities)
    │   │   └── Escalation procedures
    │   ├── 3.3 Executive Remuneration
    │   │   └── Link to climate performance metrics
    │   └── 3.4 Governance Disclosure (Draft)
    │       ├── Narrative editor (AASB S2 §6–§9 mapped)
    │       ├── Prior-year comparison pane
    │       └── Approval status + workflow
    │
    ├── 4. STRATEGY & TRANSITION
    │   ├── 4.1 Climate Risks & Opportunities Register
    │   │   ├── Add / edit risk or opportunity
    │   │   │   ├── Type (physical acute/chronic, transition category)
    │   │   │   ├── Time horizon (short / medium / long)
    │   │   │   ├── Financial effects (revenue, costs, assets, liabilities)
    │   │   │   └── Status (identified / assessed / monitored)
    │   │   └── Register table view (filter, sort, export)
    │   ├── 4.2 Scenario Analysis
    │   │   ├── Scenario configuration
    │   │   │   ├── Scenario 1 (1.5°C aligned)
    │   │   │   └── Scenario 2 (>2°C / higher warming)
    │   │   ├── Assumptions & methodology
    │   │   ├── Outputs & resilience findings
    │   │   └── Annual resilience assessment (separate from full update)
    │   ├── 4.3 Climate Transition Plan (CTP)
    │   │   ├── CTP editor (versioned)
    │   │   ├── Version history
    │   │   └── Liability protection notice (auto-displayed)
    │   └── 4.4 Strategy Disclosure (Draft)
    │       ├── Narrative editor (AASB S2 §10–§22 mapped)
    │       ├── Prior-year comparison pane
    │       └── Approval status + workflow
    │
    ├── 5. RISK MANAGEMENT
    │   ├── 5.1 Climate Risk Register
    │   │   ├── Risk entries (linked from Strategy module)
    │   │   ├── Assessment: likelihood × magnitude matrix
    │   │   ├── Control measures
    │   │   └── ERM integration statement
    │   ├── 5.2 Risk Process Documentation
    │   │   ├── Identification process description
    │   │   ├── Assessment methodology
    │   │   ├── Prioritisation criteria
    │   │   └── Monitoring frequency
    │   └── 5.3 Risk Management Disclosure (Draft)
    │       ├── Narrative editor (AASB S2 §23–§25 mapped)
    │       └── Approval status + workflow
    │
    ├── 6. EMISSIONS & ENERGY
    │   ├── 6.1 Emissions Overview (Group-level rollup)
    │   │   ├── Scope 1 total (tCO₂e)
    │   │   ├── Scope 2 total — location-based (tCO₂e)
    │   │   ├── Scope 2 total — market-based (tCO₂e)
    │   │   ├── Scope 3 total (tCO₂e) [Year 2+ mandatory]
    │   │   └── YoY comparison chart
    │   ├── 6.2 Site-Level Data Entry
    │   │   ├── Select site / reporting period
    │   │   ├── Scope 1 entry
    │   │   │   ├── Stationary combustion (fuel type, quantity, unit)
    │   │   │   ├── Mobile combustion (vehicle fleet, fuel, distance)
    │   │   │   ├── Process emissions
    │   │   │   └── Fugitive emissions
    │   │   ├── Scope 2 entry
    │   │   │   ├── Electricity (kWh, location-based factor, market-based factor)
    │   │   │   └── Purchased heat / steam / cooling
    │   │   ├── Scope 3 entry (optional Y1, mandatory Y2+)
    │   │   │   ├── Category selection (1–15 GHG Protocol categories)
    │   │   │   ├── Data input or spend-based estimation
    │   │   │   └── Methodology note
    │   │   ├── Auto-calculated CO₂e display
    │   │   ├── Supporting document upload
    │   │   └── Submit / Save as draft
    │   ├── 6.3 Emission Factors Library
    │   │   ├── NGER methodology factors (pre-loaded)
    │   │   ├── Custom factors (user-defined with justification)
    │   │   └── Factor version history
    │   └── 6.4 Emissions Disclosure (Draft)
    │       ├── Auto-populated from 6.1 data
    │       ├── Narrative editor (AASB S2 §29–§36 mapped)
    │       └── Approval status + workflow
    │
    ├── 7. METRICS & TARGETS
    │   ├── 7.1 Targets Register
    │   │   ├── Add / edit target
    │   │   │   ├── Target name & description
    │   │   │   ├── Type: mandatory (NGER) or voluntary
    │   │   │   ├── Baseline year & value
    │   │   │   ├── Target year & value
    │   │   │   └── Interim milestones
    │   │   └── Target register table
    │   ├── 7.2 Performance Tracking
    │   │   ├── Actual vs. target dashboard (per target)
    │   │   ├── Variance analysis
    │   │   └── YoY trend charts
    │   ├── 7.3 Cross-Industry Metrics
    │   │   ├── Pre-configured metric sets by industry
    │   │   └── Custom KPI builder
    │   └── 7.4 Metrics & Targets Disclosure (Draft)
    │       ├── Auto-populated from 7.1 / 7.2
    │       ├── Narrative editor (AASB S2 §37–§41 mapped)
    │       └── Approval status + workflow
    │
    ├── 8. REPORTS
    │   ├── 8.1 Sustainability Report Builder
    │   │   ├── Select reporting period
    │   │   ├── Section completeness check (must be 100% to generate)
    │   │   ├── Preview (AASB S2 paragraph index visible)
    │   │   ├── Prior-year comparison toggle
    │   │   └── Export: DOCX / PDF
    │   ├── 8.2 Assurance-Ready Data Pack
    │   │   ├── Evidence index (auto-compiled)
    │   │   ├── Calculation workpapers
    │   │   ├── Methodology notes
    │   │   └── Export as structured ZIP
    │   ├── 8.3 Executive Summary
    │   │   └── 1–2 page board-ready PDF
    │   └── 8.4 Report History
    │       └── Version archive with approval metadata
    │
    ├── 9. EVIDENCE LIBRARY
    │   ├── Upload documents
    │   ├── Tag to disclosure section
    │   ├── Document list (filter by type, section, date)
    │   └── Retention schedule tracker (7-year minimum)
    │
    ├── 10. AUDIT LOG
    │   ├── All changes log (user, field, old value, new value, timestamp)
    │   ├── Filter: by user / date range / module / field
    │   ├── Approval history
    │   └── Export log
    │
    ├── 11. NOTIFICATIONS & TASKS
    │   ├── Notification inbox (in-app)
    │   ├── Email notification preferences
    │   └── Deadline calendar
    │
    └── 12. ADMINISTRATION
        ├── Organisation settings
        ├── User & role management
        ├── Integration settings (ERP, API keys)
        ├── Emission factor library management
        └── Billing & subscription
```

---

## Navigation Hierarchy (Primary + Secondary)

### Primary Navigation (Left Sidebar — full access role)

```
[CCDS Logo]
─────────────────
  Dashboard
─────────────────
  Setup & Eligibility
  Governance
  Strategy & Transition
  Risk Management
  Emissions & Energy
  Metrics & Targets
─────────────────
  Reports
  Evidence Library
  Audit Log
─────────────────
  Notifications  [badge]
  Administration
─────────────────
  [User Avatar]
  Help & Guidance
```

### Contextual Progress Rail (per reporting period)

When inside any of the four disclosure pillars, a persistent progress rail shows:

```
Reporting Period: FY2026
─────────────────────────
● Governance         ✓ Approved
● Strategy           ⚠ In Review (2 items pending)
● Risk Management    ○ In Progress
● Metrics & Targets  ○ Not Started
─────────────────────────
Overall: 35% Complete
Deadline: 30 Sep 2026 (38 days)
```

---

## URL Structure

```
/                           → Redirect to /dashboard
/login
/eligibility-check          → Public tool (no auth)
/dashboard
/setup/company
/setup/eligibility
/setup/sites
/setup/users
/governance
/governance/board
/governance/management
/governance/remuneration
/governance/disclosure
/strategy
/strategy/risks
/strategy/scenarios
/strategy/transition-plan
/strategy/disclosure
/risk-management
/risk-management/register
/risk-management/process
/risk-management/disclosure
/emissions
/emissions/overview
/emissions/sites/:siteId
/emissions/factors
/emissions/disclosure
/metrics
/metrics/targets
/metrics/performance
/metrics/disclosure
/reports
/reports/sustainability-report
/reports/assurance-pack
/reports/executive-summary
/reports/history
/evidence
/audit-log
/notifications
/admin
/admin/users
/admin/integrations
/admin/settings
```
