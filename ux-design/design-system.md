# CCDS — Design System

A compliance tool must project **trust, clarity, and authority**. The design language is professional and restrained — not a marketing product, but also not bureaucratic. Users are stressed by deadlines and regulatory consequences; the UI should reduce that stress, not add to it.

---

## 1. Design Principles

### 1.1 Compliance Confidence
Every screen should help the user answer one question: "Am I on track?" Status indicators, progress bars, and completion checklists must be prominent and unambiguous. Never leave users unsure of their standing.

### 1.2 Contextual Guidance — Not a Manual
Regulatory complexity lives in the system, not in the user's head. Inline AASB S2 paragraph references, field-level tooltips, and contextual help panels replace the need to keep the standard open in another window.

### 1.3 Role-Appropriate Depth
A site manager sees a simple form. A CFO sees a summary. An auditor sees a trace. The same underlying data surfaces with the right level of detail for each role. Complexity is never hidden — it is positioned appropriately.

### 1.4 Earned Trust Through Auditability
The audit trail is not a back-office feature — it is a first-class interface element. Users should feel that every action is recorded, reversible via the log, and traceable. This reduces anxiety about making mistakes.

### 1.5 Calm Under Deadline Pressure
Use calm, muted colours at rest. Reserve red and amber for genuine urgency. Do not over-alert. When everything is urgent, nothing is.

---

## 2. Colour Palette

### Primary

| Token | Name | Hex | Usage |
|-------|------|-----|-------|
| `--color-primary-700` | Forest Green | `#1B5E3B` | Primary buttons, active nav, links |
| `--color-primary-500` | Sage Green | `#2E7D52` | Hover states, secondary elements |
| `--color-primary-100` | Mint Tint | `#E8F5EE` | Section backgrounds, selected states |

### Neutral (UI Foundation)

| Token | Name | Hex | Usage |
|-------|------|-----|-------|
| `--color-neutral-900` | Slate Black | `#1A1F2E` | Primary text |
| `--color-neutral-600` | Grey | `#4B5563` | Secondary text, labels |
| `--color-neutral-300` | Silver | `#D1D5DB` | Borders, dividers |
| `--color-neutral-100` | Off-White | `#F9FAFB` | Page background |
| `--color-white` | White | `#FFFFFF` | Cards, modals, panels |

### Status / Semantic

| Token | Name | Hex | Usage |
|-------|------|-----|-------|
| `--color-success-600` | Green | `#16A34A` | Approved, complete, submitted |
| `--color-success-100` | Light Green | `#DCFCE7` | Success backgrounds |
| `--color-warning-600` | Amber | `#D97706` | Overdue, in review, pending |
| `--color-warning-100` | Light Amber | `#FEF3C7` | Warning backgrounds |
| `--color-danger-600` | Red | `#DC2626` | Errors, overdue critical, rejected |
| `--color-danger-100` | Light Red | `#FEE2E2` | Error backgrounds |
| `--color-info-600` | Blue | `#2563EB` | Informational, AASB references |
| `--color-info-100` | Light Blue | `#DBEAFE` | Info backgrounds |

### Scope Emissions Coding (for charts only)

| Scope | Colour | Hex |
|-------|--------|-----|
| Scope 1 | Deep Teal | `#0F766E` |
| Scope 2 (location) | Sage | `#2E7D52` |
| Scope 2 (market) | Mint | `#6EE7B7` |
| Scope 3 | Steel Blue | `#3B82F6` |

---

## 3. Typography

**System font stack:** `Inter, -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif`

Use Inter for all UI text. Regulatory documents exported as PDF should use a serif (Georgia or similar) for legibility in print.

### Type Scale

| Token | Size | Weight | Line Height | Usage |
|-------|------|--------|-------------|-------|
| `--text-xs` | 12px | 400 | 16px | Audit log timestamps, badge labels |
| `--text-sm` | 14px | 400 | 20px | Form labels, table body, secondary text |
| `--text-base` | 16px | 400 | 24px | Body text, narrative editors |
| `--text-lg` | 18px | 500 | 28px | Section subheadings |
| `--text-xl` | 20px | 600 | 28px | Card titles, module headings |
| `--text-2xl` | 24px | 700 | 32px | Page titles |
| `--text-3xl` | 30px | 700 | 36px | Dashboard key metrics |

---

## 4. Spacing System

8px base unit. All spacing values are multiples of 4px.

```
4px   → micro gaps (between icon and label)
8px   → tight (within a form field group)
12px  → compact (between form fields)
16px  → default (between sections within a card)
24px  → comfortable (between cards)
32px  → loose (between major page sections)
48px  → section (between pillar-level blocks)
64px  → page (top-level page padding)
```

---

## 5. Component Library

### 5.1 Status Badges

Used throughout to show compliance state at a glance.

```
[● Not Started]    → grey background, neutral-600 text
[● In Progress]    → info-100 background, info-600 text
[● In Review]      → warning-100 background, warning-600 text
[● Changes Req.]   → danger-100 background, danger-600 text
[● Approved]       → success-100 background, success-600 text
[● Locked]         → neutral-100 background, neutral-900 text, lock icon
```

### 5.2 Progress Bar

Segmented bar for the 4-pillar overall progress:

```
[██████████░░░░░░░░░░] 50%    ← fills left to right
Colour: primary-500 fill on neutral-200 track
Height: 8px, border-radius: 4px
Show % text alongside
```

### 5.3 Buttons

```
Primary:    bg primary-700, white text, hover primary-500
Secondary:  border primary-700, primary-700 text, hover primary-100 bg
Danger:     bg danger-600, white text (for destructive actions)
Ghost:      no border, neutral-600 text, hover neutral-100 bg
Disabled:   neutral-300 bg, neutral-500 text, cursor not-allowed
```

All buttons: 8px padding vertical, 16px horizontal, border-radius 6px, 14px text.

### 5.4 Form Fields

```
Label:        text-sm, neutral-900, weight 500, 8px below
Input:        full width, border neutral-300, 8px padding, border-radius 6px
Focus:        border primary-500, box-shadow 0 0 0 3px primary-100
Error:        border danger-600, error message below in danger-600 text-sm
Tooltip (ℹ️): icon next to label, hover shows popover with AASB S2 context
```

### 5.5 Data Table

```
Header:     neutral-100 bg, text-sm, weight 600, neutral-600 colour
Body rows:  white bg, border-bottom neutral-200, text-sm neutral-900
Hover row:  primary-100 bg
Sortable:   up/down caret icon on sortable columns
Actions:    right-aligned, ghost buttons per row
Sticky:     first column sticky on horizontal scroll (mobile)
```

### 5.6 Cards

```
Background:    white
Border:        1px neutral-200
Border-radius: 8px
Padding:       24px
Shadow:        0 1px 3px rgba(0,0,0,0.08)
```

### 5.7 Contextual Help Panel (AASB Reference)

Appears as a fixed right panel (320px wide) when inside any disclosure section:

```
┌──────────────────────────┐
│  AASB S2 GUIDANCE        │
│  ─────────────────────── │
│  §7(a) Governance        │
│                          │
│  "An entity shall        │
│  disclose information    │
│  about the governance    │
│  body(ies)..."           │
│                          │
│  Mandatory: Yes          │
│  Assurance (Yr 1): Yes   │
│                          │
│  [Read full paragraph ↗] │
└──────────────────────────┘
```

### 5.8 Notification Toast

Appears at top-right, auto-dismisses after 5s:

```
✅ Success:  green-700 left border, white bg
⚠️ Warning:  amber-600 left border, white bg
❌ Error:    red-600 left border, white bg
ℹ️ Info:    blue-600 left border, white bg
```

### 5.9 Liability Protection Banner

Displayed automatically on Scope 3, CTP, and Scenario Analysis screens during FY2025–FY2027:

```
┌──────────────────────────────────────────────────────────────────┐
│ 🛡️  MODIFIED LIABILITY PROTECTION APPLIES                        │
│   Disclosures in this section are covered by the modified        │
│   liability regime under the Corporations Act for FY2025–2027.   │
│   Civil litigation immunity applies to forward-looking           │
│   statements. See legal guidance for details.                    │
└──────────────────────────────────────────────────────────────────┘
Colour: info-100 background, info-600 border-left 4px, info-600 text
```

---

## 6. Layout Grid

**Desktop (≥1280px):** 12-column grid, 24px gutters, 64px side padding
**Tablet (768–1279px):** 8-column grid, 16px gutters
**Mobile (<768px):** 4-column grid, 16px gutters, full-width cards

### Application Shell Layout

```
┌──────────────────────────────────────────────────────────────────┐
│  TOP BAR (64px height)                                           │
│  Logo | Org name | Period selector | Notification | Avatar       │
├─────────────┬────────────────────────────────────────────────────┤
│             │                                                    │
│  LEFT NAV   │   MAIN CONTENT AREA                               │
│  (240px)    │   (flex, full height)                             │
│             │                                                    │
│  Fixed on   │   Optional: RIGHT PANEL (320px)                   │
│  desktop    │   AASB guidance / evidence / audit trail          │
│             │                                                    │
│  Collapses  │                                                    │
│  to icons   │                                                    │
│  on tablet  │                                                    │
│             │                                                    │
└─────────────┴────────────────────────────────────────────────────┘
```

---

## 7. Iconography

Use [Lucide](https://lucide.dev/) icon set (MIT licensed, consistent stroke-width style).

| Icon | Usage |
|------|-------|
| `shield-check` | Governance, compliance confirmed |
| `leaf` | Emissions, sustainability |
| `triangle-alert` | Risk, warning |
| `target` | Targets, KPIs |
| `file-text` | Reports, documents |
| `folder-open` | Evidence library |
| `scroll-text` | Audit log |
| `bell` | Notifications |
| `lock` | Locked/final state |
| `unlock` | Editable state |
| `circle-check` | Approved, complete |
| `clock` | Pending, deadline |
| `upload` | Evidence upload |
| `link` | Trace/link to source |
| `chevron-right` | Navigation, expandable rows |

All icons: 20px × 20px in nav, 16px × 16px inline. Stroke width: 1.5px. Colour inherits from text.

---

## 8. Motion & Transitions

Keep transitions fast and purposeful. This is a productivity tool, not a marketing site.

| Element | Property | Duration | Easing |
|---------|----------|----------|--------|
| Sidebar collapse | width | 200ms | ease-in-out |
| Modal open | opacity + translateY | 150ms | ease-out |
| Toast appear | opacity + translateX | 150ms | ease-out |
| Status badge change | background-color | 100ms | ease |
| Progress bar fill | width | 400ms | ease-out |
| Hover states (buttons, rows) | background | 80ms | ease |

No animations for data loads — use a skeleton screen instead of a spinner where possible.

---

## 9. Responsive Behaviour Notes

### Mobile (site manager primary target)
- Left nav collapses to bottom tab bar (max 5 items): Dashboard, Tasks, Emissions, Evidence, More
- All data entry forms are single-column
- File upload via camera (for utility bills) enabled on mobile
- Scope 3 section collapsed by default with "Optional in Year 1" banner
- CO₂e totals shown prominently after each input field

### Tablet (ESG manager secondary)
- Left nav collapses to icon-only (64px)
- Tables switch to horizontal scroll with sticky first column
- Right guidance panel becomes a slide-out overlay

### Accessibility
- WCAG 2.1 AA minimum
- All colour usage meets 4.5:1 contrast ratio (text) / 3:1 (UI components)
- All interactive elements keyboard-navigable
- All form fields have associated `<label>` elements
- Status conveyed by more than colour alone (icon + text always paired with colour)
- Audit log and data tables support screen readers with proper `<th scope>` and ARIA roles

---

## 10. Empty States

Every module needs a well-designed empty state — particularly at first setup.

```
Governance (empty):
  [governance icon — large, outlined]
  "No governance information recorded yet."
  "Document your board's climate oversight to satisfy AASB S2 §6–§9."
  [Add board committee]

Risk Register (empty):
  [shield icon — large, outlined]
  "Your climate risk register is empty."
  "Identifying and documenting risks is required under AASB S2 §23."
  [Add first risk]   [Import from ERM system]

Emissions (site, empty):
  [leaf icon]
  "No emissions data for this period."
  [Enter data]   [Import CSV]
```

Empty states always include: a contextual icon, a plain-English explanation, the AASB S2 requirement behind it, and a clear call-to-action.
