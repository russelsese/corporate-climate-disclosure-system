# Business Requirements: Corporate Climate Disclosure System (CCDS)

**Document Status:** Initial Draft
**Date:** 2026-03-04
**Version:** 0.1

---

## 1. Background & Regulatory Context

### 1.1 Legislation

Australia's **Treasury Laws Amendment (Financial Market Infrastructure and Other Measures) Act 2024** received Royal Assent on 17 September 2024, amending the *Corporations Act 2001* to introduce mandatory climate-related financial disclosures. Compliance is enforced by ASIC under **Regulatory Guide 280** (March 2025).

The governing disclosure standard is **AASB S2 Climate-related Disclosures** (September 2024), which aligns with the International Sustainability Standards Board (ISSB) IFRS S2 framework.

### 1.2 Who Must Report

Entities lodging financial reports under Chapter 2M of the Corporations Act must comply if they meet **at least 2 of 3** size criteria within their group:

| Group | Revenue (consolidated) | Gross Assets (consolidated) | Employees | Reporting Start |
|-------|----------------------|----------------------------|-----------|-----------------|
| **Group 1** | ≥ AUD $500M | ≥ AUD $1B | ≥ 500 | FY beginning on/after 1 Jan 2025 |
| **Group 2** | ≥ AUD $200M | ≥ AUD $500M | ≥ 100 | FY beginning on/after 1 Jul 2026 |
| **Group 3** | ≥ AUD $50M | ≥ AUD $25M | ≥ 50 | FY beginning on/after 1 Jul 2027 |

**Additionally**, any entity that is an NGER (National Greenhouse and Energy Reporting) controlling corporation is automatically in scope regardless of size thresholds.

### 1.3 What Must Be Disclosed

AASB S2 requires a **Sustainability Report** covering four core disclosure pillars (TCFD-aligned):

1. **Governance** — How the board and management oversee and manage climate-related risks and opportunities.
2. **Strategy** — Material climate risks and opportunities, their anticipated financial effects, and the entity's Climate Transition Plan (CTP).
3. **Risk Management** — Processes for identifying, assessing, prioritising, and monitoring climate risks, integrated with enterprise risk management.
4. **Metrics & Targets** — GHG emissions (Scope 1, 2, and 3), climate-related targets, and progress tracking.

**Scope 3 emissions** are mandatory from the entity's **second reporting year** (Year 1 exemption applies).

**Scenario Analysis** — Entities must assess climate resilience annually and update full scenario analysis aligned with their strategic planning cycle. At minimum, a 1.5°C pathway and a higher warming scenario must be modelled.

### 1.4 Assurance Requirements (ASSA 5010)

All disclosures are subject to external assurance under a staged pathway:

| Year of Reporting | Assurance Level | Scope |
|-------------------|----------------|-------|
| Year 1 | Limited assurance | Governance, Strategy, Scope 1 & 2 emissions |
| Year 2 | Limited assurance | Adds Scope 3 emissions |
| Year 3 | Limited assurance | Full sustainability report |
| Year 4+ | **Reasonable assurance** | Full sustainability report (audit-grade) |

### 1.5 Liability Protection

For FY 2025–2027, a **modified liability regime** grants civil litigation immunity for disclosures relating to:
- Scope 3 GHG emissions
- Scenario analysis outputs
- Climate Transition Plans (CTPs)

---

## 2. Business Objectives

The Corporate Climate Disclosure System (CCDS) must enable Australian companies to:

1. Determine whether they are a reporting entity (eligibility assessment).
2. Collect, validate, and consolidate climate-related data across sites, subsidiaries, and supply chains.
3. Prepare AASB S2-compliant Sustainability Reports within required deadlines.
4. Maintain an auditable evidence trail sufficient to satisfy ASSA 5010 assurance requirements.
5. Track year-on-year progress against declared climate targets and KPIs.
6. Support board and management governance reporting obligations.

---

## 3. Stakeholders

| Stakeholder | Role |
|-------------|------|
| CFO / Finance Team | Report owner; responsible for lodging the Sustainability Report |
| Board / Audit & Risk Committee | Governance oversight; approves disclosures |
| Sustainability / ESG Team | Primary data owners and report preparers |
| Operations / Site Managers | Data contributors (energy, emissions, waste) |
| External Auditor | Performs ASSA 5010 assurance engagement |
| ASIC | Regulatory body; enforces compliance |
| Legal / Company Secretary | Manages Corporations Act lodgement obligations |

---

## 4. Functional Requirements

### 4.1 Eligibility Assessment

- **BR-001** The system shall allow a company to input its consolidated revenue, gross assets, and employee count to determine which Group (1, 2, or 3) it falls into and its first mandatory reporting date.
- **BR-002** The system shall flag NGER controlling corporations as automatically in scope.
- **BR-003** The system shall handle group structures (parent + subsidiaries) and assess eligibility at the consolidated level.

### 4.2 Governance Module

- **BR-004** The system shall capture and record board-level climate governance structures (committee names, charters, meeting frequency, oversight activities).
- **BR-005** The system shall record management-level roles and responsibilities for climate risk and opportunity management.
- **BR-006** The system shall store evidence documents (board minutes, committee charters, policy documents) linked to governance disclosures.
- **BR-007** The system shall track how climate considerations are integrated into executive remuneration.

### 4.3 Strategy & Transition Planning

- **BR-008** The system shall allow users to document identified climate-related risks and opportunities across short, medium, and long-term time horizons.
- **BR-009** The system shall capture the anticipated financial effects (quantitative and qualitative) of each risk/opportunity on revenue, costs, assets, and liabilities.
- **BR-010** The system shall provide a structured module for authoring and version-controlling the Climate Transition Plan (CTP).
- **BR-011** The system shall support at least two scenario inputs (e.g., 1.5°C-aligned and ≥2°C warming), capturing assumptions, methodology, and outputs.
- **BR-012** The system shall record annual resilience assessments separately from full scenario analysis updates.

### 4.4 Risk Management

- **BR-013** The system shall maintain a climate risk register, allowing categorisation by type (physical: acute/chronic; transition: policy, legal, technology, market, reputational).
- **BR-014** The system shall capture risk assessment inputs: likelihood, magnitude, time horizon, and control measures.
- **BR-015** The system shall document how the climate risk management process integrates with the entity's broader enterprise risk management (ERM) framework.

### 4.5 Emissions & Energy Data Capture

- **BR-016** The system shall capture Scope 1 (direct), Scope 2 (purchased energy), and Scope 3 (value chain) GHG emissions data.
- **BR-017** The system shall support data entry at the site/facility level and roll up to entity and group level.
- **BR-018** The system shall record emission factors, methodologies, and data sources used in calculations (aligned to NGER methodology where applicable).
- **BR-019** The system shall support both location-based and market-based methods for Scope 2 reporting.
- **BR-020** The system shall calculate and display total GHG emissions in CO₂-equivalent (tCO₂e).
- **BR-021** Scope 3 data entry shall be flagged as optional in Year 1 but mandatory from Year 2 onwards.
- **BR-022** The system shall maintain a full audit log of data entries, edits, and approvals for assurance purposes.

### 4.6 Metrics & Targets

- **BR-023** The system shall allow the entity to define and track climate-related targets (e.g., net-zero by 2050, 50% Scope 1 reduction by 2030).
- **BR-024** The system shall track year-on-year actual performance against each target and display variance.
- **BR-025** The system shall capture legally mandated targets (e.g., NGER obligations) separately from voluntary targets.
- **BR-026** The system shall support cross-industry metric sets and allow custom KPIs defined by the entity.

### 4.7 Report Generation

- **BR-027** The system shall generate a structured draft Sustainability Report in a format suitable for inclusion in (or alongside) the Annual Report.
- **BR-028** The report output shall map all disclosures explicitly to the relevant AASB S2 paragraph references.
- **BR-029** The system shall support comparative period reporting (current year vs. prior year).
- **BR-030** The system shall produce an assurance-ready data pack (supporting evidence, calculation workpapers, methodology notes) for external auditors.

### 4.8 Workflow & Approvals

- **BR-031** The system shall support a structured review and approval workflow (preparer → reviewer → approver) for each disclosure section.
- **BR-032** The system shall provide a checklist/status dashboard showing completion status across all four pillars.
- **BR-033** The system shall send notifications/reminders to assigned users when data is due or approvals are pending.

---

## 5. Non-Functional Requirements

| Category | Requirement |
|----------|-------------|
| **Security** | Role-based access control (RBAC); separation between data contributors, preparers, and approvers |
| **Audit Trail** | Immutable log of all data changes with user, timestamp, and reason for change |
| **Data Retention** | Retain all disclosure data and supporting evidence for a minimum of 7 years |
| **Integration** | API or import capability for ERP systems (energy billing, asset registers, payroll headcount) |
| **Accessibility** | Must be accessible via web browser; mobile-friendly for site-level data entry |
| **Multi-entity** | Must support group structures with multiple legal entities and consolidation |

---

## 6. Out of Scope (Initial Release)

- General sustainability reporting beyond climate (AASB S1 voluntary disclosures)
- Carbon credit/offset management and trading
- Supplier/third-party portal for Scope 3 data collection (future phase)
- Integration with stock exchange lodgement platforms (future phase)

---

## 7. Key Regulatory References

- [AASB S2 Climate-related Disclosures (Sep 2024)](https://standards.aasb.gov.au/aasb-s2-sep-2024)
- [Treasury Laws Amendment (Financial Market Infrastructure and Other Measures) Act 2024](https://www.allens.com.au/insights-news/insights/2024/09/mandatory-climate-related-financial-reporting-legislation/)
- [ASIC Regulatory Guide 280 – Sustainability Reporting (March 2025)](https://download.asic.gov.au/media/j4rhwyiz/rg280-published-31-march-2025.pdf)
- [ASSA 5010 – Assurance Timeline Standard](https://auasb.gov.au/media/wf5frdj0/assa5010.pdf)
- [AASB Overview of Australian Sustainability Reporting Standards](https://aasb.gov.au/media/xpilzp2e/overviewofasrs_04-25.pdf)
- [ASIC Media Release – Prepare for Mandatory Climate Reporting](https://www.asic.gov.au/about-asic/news-centre/find-a-media-release/2024-releases/24-205mr-asic-urges-businesses-to-prepare-for-mandatory-climate-reporting/)
