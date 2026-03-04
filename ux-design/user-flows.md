# CCDS — User Flows

Key journeys mapped end-to-end. Notation: rectangles = screens, diamonds = decisions, cylinders = data stores, rounded = start/end.

---

## Flow 1: New Company Onboarding & Eligibility Check

**Persona:** ESG Manager (Sarah) setting up for the first time
**Trigger:** Company decides to implement CCDS

```
(START)
   │
   ▼
[Public: Eligibility Check Tool]
  Enter: Revenue / Assets / Employees / NGER status
   │
   ◆ Meets 2 of 3 thresholds OR is NGER?
   │
  YES──────────────────────────────────────────────────────────────NO──────────────┐
   │                                                                                │
   ▼                                                                                ▼
[Result: Group 1 / 2 / 3 + first reporting date]               [Result: Not currently required]
[CTA: "Set up your account"]                                   [CTA: "Save result / check again next year"]
   │                                                                                │
   ▼                                                                               (END)
[Register Account]
  Enter: Name / Work email / Organisation / ABN
   │
   ▼
[Email verification + MFA setup]
   │
   ▼
[Onboarding Wizard — Step 1: Company Profile]
  Company name, ABN, ACN, industry sector, financial year end
   │
   ▼
[Step 2: Group Structure]
  ◆ Is this a group with subsidiaries?
  YES → Add subsidiary entities (repeat per entity)
  NO  → Continue
   │
   ▼
[Step 3: Reporting Period]
  Confirm first mandatory reporting period
  Set internal reporting deadlines (data due, draft due, board approval due)
   │
   ▼
[Step 4: Sites & Facilities]
  Add facilities (name, address, site type)
  Assign a site manager per facility
   │
   ▼
[Step 5: Invite Team]
  Invite users by email
  Assign role: ESG Manager / CFO / Site Manager / Board Director / Auditor / Legal
   │
   ▼
[Setup Complete — Go to Dashboard]
   │
   ▼
(END)
```

---

## Flow 2: Annual Reporting Cycle (ESG Manager)

**Persona:** Sarah (ESG Manager)
**Trigger:** New financial year begins; reporting period opens

```
(START — Reporting period opens)
   │
   ▼
[Dashboard shows: new reporting period active]
[Checklist: 4 pillars, all "Not Started"]
   │
   ▼
[Assign tasks to site managers for emissions data]
  Set due dates per site
  Notifications sent automatically
   │
   ▼
[Work on Governance section]
  → Enter board committee details
  → Log oversight activities
  → Upload board minutes / charter evidence
  → Write governance narrative
  → Submit for CFO review
   │
   ▼
[Work on Strategy section]
  → Enter climate risks and opportunities
  → Add financial effects per risk/opportunity
  → Run scenario analysis (1.5°C + higher warming)
  → Draft Climate Transition Plan
  → Write strategy narrative
  → Submit for CFO review
   │
   ▼
[Work on Risk Management section]
  → Confirm risk register entries (linked from Strategy)
  → Document risk process
  → Write risk management narrative
  → Submit for CFO review
   │
   ▼
[Monitor site emissions submissions]
  ◆ All sites submitted?
  NO → Send reminders / follow up
  YES → Continue
   │
   ▼
[Review and approve site-level data]
  Check for outliers / anomalies
  Confirm emission factors applied correctly
  Approve rollup to entity/group total
   │
   ▼
[Work on Metrics & Targets section]
  → Confirm/update target register
  → Review actual vs. target performance
  → Write metrics narrative
  → Submit for CFO review
   │
   ▼
[All 4 pillars submitted for review]
   │
   ▼
[CFO reviews and approves each pillar]  ←── (see Flow 4)
   │
   ▼
[Generate Sustainability Report]
  Preview → finalise → export PDF/DOCX
   │
   ▼
[Generate Assurance-Ready Data Pack]
  Export for external auditor
   │
   ▼
[Legal / Company Secretary final review]  ←── (see Flow 5)
   │
   ▼
[Report locked and lodged]
   │
   ▼
(END)
```

---

## Flow 3: Site-Level Emissions Data Entry (Site Manager)

**Persona:** David Park (Site Operations Manager)
**Trigger:** Notification received: "Emissions data due for [Site Name] by [Date]"

```
(START — notification received via email / in-app)
   │
   ▼
[Open notification → lands on Site Emissions Entry screen]
  Header: "Q4 2025 Emissions — Dandenong Plant"
  Deadline displayed: "Due in 12 days"
   │
   ▼
[Scope 1 — Stationary Combustion]
  ◆ Do you use natural gas?  [Yes/No toggle]
  YES → Enter: Volume (GJ or m³) + meter read dates
  ◆ Do you use diesel/petrol?
  YES → Enter: Litres consumed + purpose
  System auto-displays: calculated tCO₂e per source
   │
   ▼
[Scope 1 — Mobile Combustion]
  ◆ Company vehicles on site?
  YES → Enter: vehicle type / fuel / litres or km
   │
   ▼
[Scope 2 — Electricity]
  Enter: kWh consumed (from utility bill)
  Upload utility bill as evidence [drag & drop]
  System auto-calculates:
    Location-based CO₂e (NGER grid factor)
    Market-based CO₂e (if renewable certificate data entered)
   │
   ▼
[Scope 3 — Value Chain]
  [BADGE: Optional in Year 1 — Mandatory from Year 2]
  ◆ Skip for now?
  YES → Continue
  NO  → Select category → enter data
   │
   ▼
[Summary screen]
  Total Scope 1: XX tCO₂e
  Total Scope 2 (location): XX tCO₂e
  Total Scope 2 (market): XX tCO₂e
  Scope 3: Not entered / XX tCO₂e
  Supporting documents: [listed]
  ◆ Everything look right?
   │
   ├──NO → [Go back and edit]
   │
   └──YES ↓
   │
   ▼
[Submit]
   │
   ▼
[Confirmation screen]
  "Submitted successfully ✓"
  "Your ESG Manager will review and confirm."
  "Reference: SITE-DAN-Q4-2025"
   │
   ▼
[Notification sent to Sarah (ESG Manager)]
   │
   ▼
(END)
```

---

## Flow 4: Approval Workflow (CFO)

**Persona:** Alex Chen (CFO)
**Trigger:** Notification: "Governance section ready for your approval"

```
(START — notification received)
   │
   ▼
[Open notification → lands on Approval screen for Governance]
   │
   ▼
[Section Summary view]
  AASB S2 pillar: Governance
  Prepared by: Sarah Mitchell
  Submitted: [date]
  Status: Pending CFO Approval
   │
   ▼
[Read narrative disclosure]
  Side panel: AASB S2 paragraph references
  Prior-year comparison available (toggle)
   │
   ▼
[Review supporting evidence list]
  (links to board minutes, charter PDFs)
   │
   ◆ Satisfied?
   │
  NO ──────────────────────────────────────────────YES
   │                                                 │
   ▼                                                 ▼
[Request Changes]                           [Approve section]
  Enter comment                             Enter digital signature / PIN
  → Section status: "Changes Requested"     → Section status: "CFO Approved ✓"
  → Sarah notified                          → Next approver notified (Board if required)
   │                                                 │
   ▼                                                 ▼
[Sarah revises + resubmits]                [Board Director notified if governance]
   │                                                 │
   └──────────────────────────────────────►(END of this approval loop)
```

---

## Flow 5: Auditor Access & Evidence Trace

**Persona:** Marcus Thompson (External Auditor)
**Trigger:** Sarah grants Marcus time-limited auditor access

```
(START — auditor receives access invitation)
   │
   ▼
[Login → Auditor Portal view]
  Scoped to: FY2026 reporting period only
  Read-only badge visible on all screens
   │
   ▼
[Audit Overview Dashboard]
  Sections in scope per ASSA 5010 (Year 1 or 2 or 3 assurance scope displayed)
  Status of each section: Approved / Pending
   │
   ▼
[Navigate to Emissions & Energy → Scope 1]
   │
   ▼
[View disclosed Scope 1 figure: 1,240 tCO₂e]
  Click "Trace this figure"
   │
   ▼
[Calculation breakdown]
  Dandenong Plant: 620 tCO₂e
    └── Natural gas: 4,800 GJ × 51.53 kgCO₂e/GJ = 247 tCO₂e
    └── Diesel (mobile): 28,000L × 2.68 kgCO₂e/L = 75 tCO₂e
    └── Source: NGER Measurement Determination 2024, Table 1
  Footscray Office: 620 tCO₂e
    └── [similar detail]
   │
   ▼
[Click "View source document"]
  → Opens utility bill / invoice PDF uploaded by David
   │
   ▼
[Click "View emission factor"]
  → Opens NGER factor table with version reference
   │
   ▼
[Raise a Query]
  Enter: "Diesel consumption at Dandenong seems high vs. prior year. Please clarify."
  → Sarah notified
  → Query tracked in Audit Queries thread
   │
   ▼
[Sarah responds with explanation]
  → Marcus sees response, closes query
   │
   ▼
[Export full evidence pack as ZIP]
   │
   ▼
(END)
```

---

## Flow 6: Report Generation & Lock

**Persona:** Sarah (ESG Manager) + Lisa (Company Secretary)
**Trigger:** All 4 pillars are CFO-approved

```
(START — all pillars show "Approved" status)
   │
   ▼
[Reports → Sustainability Report Builder]
  Select period: FY2026
  Completeness check: 4/4 sections approved ✓
   │
   ▼
[Preview mode]
  Full Sustainability Report rendered
  AASB S2 paragraph index in right panel
  Prior-year comparison toggle (on/off)
   │
   ▼
[Lisa reviews final report]
  Checks mandatory vs optional disclosure completeness
  Verifies liability protection notices on Scope 3 / CTP / scenario analysis
   │
   ◆ Any issues?
  YES → raise change request (creates amendment workflow, new version)
  NO ↓
   │
   ▼
[Lisa: "Finalise Report"]
  Report locked (version 1.0 — FY2026)
  Timestamp + approval metadata embedded
  Change-lock activated (any further edit requires formal amendment)
   │
   ▼
[Export options]
  PDF (Sustainability Report — ready for Annual Report inclusion)
  DOCX (editable for layout team)
  Assurance Pack ZIP (for Marcus)
  Executive Summary PDF (for board)
   │
   ▼
[Report archived in Report History]
  Status: Final | Lodgement ready
   │
   ▼
(END)
```

---

## Flow 7: Notifications & Deadline Management

**Trigger:** System-generated based on configured deadlines

```
Automated notification events:
  ├── [D-30] "Site emissions data due in 30 days" → Site Managers
  ├── [D-14] "Emissions data overdue for [Site]" → ESG Manager + Site Manager
  ├── [D-0]  "Section submitted for your review" → Reviewer
  ├── [Approval] "Changes requested on [Section]" → Preparer
  ├── [Approval] "[Section] approved by CFO" → ESG Manager + Legal
  ├── [D-30] "Sustainability Report deadline in 30 days" → CFO + Legal
  └── [Auditor] "Auditor raised a query on [Section]" → ESG Manager

Notification delivery:
  ├── In-app notification inbox (bell icon, badge count)
  ├── Email (summary digest: immediate / daily / weekly — user preference)
  └── Deadline calendar (iCal export available)
```

---

## State Transitions — Disclosure Section Status

Each of the four disclosure pillars moves through these states:

```
[Not Started]
    │
    │ ESG Manager begins work
    ▼
[In Progress]
    │
    │ ESG Manager submits for review
    ▼
[In Review — Pending CFO]
    │
    ├── CFO requests changes ──► [Changes Requested] ──► [In Review — Pending CFO]
    │
    │ CFO approves
    ▼
[CFO Approved]
    │
    │ (For Governance only) Board Director approval required
    ▼
[Board Approved]  (or stays at CFO Approved for other pillars)
    │
    │ Report generated and locked
    ▼
[Locked — Final]
    │
    │ Amendment required post-lock
    ▼
[Amendment In Progress] ──► (restarts approval chain)
```
