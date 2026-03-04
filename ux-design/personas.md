# CCDS — User Personas

Six distinct user types interact with the system. Each has different goals, technical comfort levels, and access needs. Designs must serve all of them without sacrificing simplicity for any.

---

## Persona 1: Alex Chen — CFO / Finance Lead

**Age:** 47 | **Organisation:** Large listed company (Group 1) | **Tech comfort:** Medium

**Context**
Alex is the report owner. His name goes on the Sustainability Report lodged with ASIC. He is accountable to the board and to auditors. He doesn't build the data — he reviews, approves, and signs off.

**Primary Goals**
- Get a single-view "is this compliant?" answer at any point in time
- Approve disclosures quickly without re-reading mountains of raw data
- Download a board-ready executive summary before audit season

**Pain Points**
- Chasing ESG teams for status updates via email
- Not knowing which sections are blocked until a deadline is approaching
- Uncertainty about whether Scope 3 data meets the assurance threshold

**How he uses the system**
- Logs in weekly during reporting season to check the dashboard
- Reviews and approves completed sections in the approval workflow
- Downloads the draft Sustainability Report for board pre-read
- Checks the audit-readiness indicator before engaging the external auditor

**Key Design Needs**
- High-level dashboard with clear red/amber/green status per pillar
- One-click approval with optional comment
- Mobile-accessible so he can approve during board meetings
- Deadline countdown always visible

---

## Persona 2: Sarah Mitchell — ESG / Sustainability Manager

**Age:** 36 | **Organisation:** Mid-size company (Group 2) | **Tech comfort:** High

**Context**
Sarah is the primary power user. She manages the full reporting cycle: collecting data from sites, writing narrative disclosures, running scenario analysis, and preparing the draft report. She uses the system daily during reporting windows.

**Primary Goals**
- Complete all four disclosure pillars accurately and on time
- Avoid duplicate data entry — import where possible
- Track which site managers have submitted vs. are outstanding

**Pain Points**
- Emission factor version changes mid-year causing re-calculations
- Site managers submitting data in wrong formats
- Not knowing which AASB S2 paragraph a disclosure maps to

**How she uses the system**
- Full access across all modules
- Sets up the reporting period and assigns tasks to site managers
- Writes governance, strategy, and risk narrative
- Reviews site-level emissions submissions and approves roll-up
- Generates the draft Sustainability Report and assurance-ready pack

**Key Design Needs**
- Task management view showing outstanding items by person
- In-system guidance linking each field to the AASB S2 paragraph it satisfies
- Bulk import for emissions data (CSV/Excel)
- Side-by-side prior-year comparison when drafting narrative
- Clear "assurance scope" indicator per section (Year 1/2/3/4)

---

## Persona 3: David Park — Site Operations Manager

**Age:** 41 | **Organisation:** Manufacturing plant, part of Group 1 entity | **Tech comfort:** Low–Medium

**Context**
David manages one of eight manufacturing facilities. He is responsible for submitting energy and emissions data for his site each quarter. He is not a climate expert — he just knows his electricity bills, fuel consumption, and waste figures.

**Primary Goals**
- Enter site data quickly and correctly
- Know what he needs to submit and by when
- Not get called up by Sarah asking why he hasn't submitted yet

**Pain Points**
- Forms that ask for jargon he doesn't understand (e.g., "GWP-weighted CO₂e")
- Uploading spreadsheets that get rejected for formatting errors
- No confirmation that his submission was received and accepted

**How he uses the system**
- Primarily on a tablet or mobile at the factory floor
- Receives a task notification → opens the app → enters meter readings and fuel purchases
- Uploads utility bills as supporting evidence
- Submits and gets a confirmation receipt

**Key Design Needs**
- Extremely simple mobile-first data entry — plain English labels, no jargon
- Tooltips explaining what each field means
- Auto-calculation of CO₂e from raw inputs (litres of diesel, kWh of electricity)
- Upload utility bills/invoices as supporting documents
- Clear submission confirmation and status ("Submitted — awaiting review")
- Offline capability or save-as-draft for low-connectivity environments

---

## Persona 4: Jennifer Walsh — Board Director / Audit & Risk Committee Chair

**Age:** 58 | **Organisation:** ASX-listed Group 1 entity | **Tech comfort:** Low

**Context**
Jennifer chairs the Board's Audit & Risk Committee. She needs to be able to demonstrate to ASIC that the board oversaw and approved climate disclosures. She rarely logs in herself — she reviews a board pack prepared from the system.

**Primary Goals**
- See an executive-level summary of climate risk exposure and disclosure status
- Confirm the board's oversight activities are formally recorded
- Sign off on the governance section before it goes to the auditor

**Pain Points**
- Receiving 80-page PDFs when she only needs a one-page summary
- Not having a clear record of which board meetings discussed climate risk
- Uncertainty about personal director liability for disclosure errors

**How she uses the system**
- Logs in a few times per year (pre-board meetings, at approval milestones)
- Views the governance calendar and confirms board oversight activities are recorded
- Reads and approves the Governance disclosure section
- Downloads a 1–2 page executive summary for the board pack

**Key Design Needs**
- Executive dashboard: stripped back, narrative-first, large typography
- Governance calendar view showing recorded oversight activities
- One-click governance section approval with digital signature capture
- Printable / PDF-exportable executive summary
- Liability protection notice visible on Scope 3 and scenario analysis screens

---

## Persona 5: Marcus Thompson — External Auditor

**Age:** 39 | **Organisation:** Big 4 audit firm | **Tech comfort:** High

**Context**
Marcus conducts the ASSA 5010 limited assurance engagement. He doesn't enter or edit data — he reads, queries, and traces every number back to its source. His access is read-only but deep.

**Primary Goals**
- Trace each disclosed figure back to its source data and methodology
- Access all supporting evidence (utility bills, board minutes, emission factor tables)
- Raise queries when data looks inconsistent and track responses

**Pain Points**
- Being given a spreadsheet with no audit trail
- Evidence documents not linked to the specific disclosure they support
- Calculation methodologies not documented within the system

**How he uses the system**
- Granted time-limited read-only access to a specific reporting period
- Navigates the assurance-ready data pack
- Drills from a disclosed figure → emission calculation → source document
- Raises audit queries that go to Sarah (ESG Manager) for response
- Views the full audit log (who entered what, when, what changed)

**Key Design Needs**
- Auditor portal with scoped read-only access (by reporting period)
- Evidence trace: figure → calculation → methodology → source document (one click chain)
- Audit log viewer with filtering by date, user, field
- Raise query feature with threaded response tracking
- AASB S2 paragraph mapping visible on every disclosure
- Export full evidence pack as a structured ZIP/PDF

---

## Persona 6: Lisa Nguyen — Company Secretary / Legal Counsel

**Age:** 43 | **Organisation:** Group 1 entity | **Tech comfort:** Medium

**Context**
Lisa manages compliance deadlines, lodgement with ASIC, and ensures the Sustainability Report is legally sound. She is particularly focused on the liability protection provisions and deadline management.

**Primary Goals**
- Know exactly when the Sustainability Report must be lodged
- Ensure liability protection disclosures (Scope 3, CTP, scenario analysis) are correctly worded
- Have a signed-off, final report ready to lodge

**Pain Points**
- Last-minute changes to the report after legal review that break the audit trail
- Not knowing whether required AASB S2 disclosures are complete vs. optional
- Having to manually check liability protection clause applicability each year

**How she uses the system**
- Reviews the compliance checklist against AASB S2 mandatory vs. optional disclosures
- Checks the liability protection flag on Scope 3, CTP, and scenario analysis sections
- Exports the final, approved Sustainability Report for lodgement
- Monitors the reporting deadline calendar

**Key Design Needs**
- Compliance checklist clearly marked mandatory vs. optional per AASB S2
- Liability protection badge displayed on relevant disclosure sections
- Deadline calendar with ASIC lodgement dates and internal milestones
- Final report export with version number and approval audit trail embedded
- Change-lock mechanism: once approved, changes require a formal amendment workflow
