---
name: top-line
description: Use this skill whenever Michele asks to build or populate the Top Line tab of a PLAN workbook — for any client, any engagement. Triggers on phrases like "let's do the top line," "fill in the revenue tab," "build the channel breakdown," or any request to translate persona revenue targets into channel and geography figures. Always complete Customer Objectives and Brand Objectives first — Top Line is a reconciliation output, not a starting point. Assumes an empty sheet and an existing Bridge tab unless told otherwise.
---

# Top Line Tab — Build Process

The Top Line tab translates persona-level revenue targets into channel and geography breakdowns. It is the reconciliation layer — the point where customer strategy meets commercial reality. Every figure in the Top Line must be traceable back to a persona assumption in Customer Objectives. It is not built independently.

---

## What It Is Not

- Not a starting point. Top Line is built after Customer Objectives and Brand Objectives are locked. Never build Top Line first.
- Not a set of independent estimates. Every channel and geography figure derives from persona revenue multiplied by allocation assumptions in the Bridge tab. Figures that cannot be traced back to a persona assumption do not belong here.
- Not static. Channel mix and geography allocations change year by year as the business evolves, new channels open, and new markets activate. Static allocations across all years are wrong.

---

## Tab Structure

Two sections, each breaking the total business a different way:

**By Channel** — how product and services reach customers:
- Define channels based on how this specific business actually operates
- Standard channel types to consider: Online (DTC), Physical Location, Atelier/Events, Fairs, B2B Material, B2B Service, B2C Material, B2C Service
- Add or remove channels based on the client's actual business model — do not import a template channel list without validating it against reality
- B2C Material is typically a subtotal (Online + Atelier/Events + Fairs) — make this explicit in the tab
- Service channels (B2B Service, B2C Service) may be zero at the start — that is correct if they do not yet exist

**By Geography** — where revenue originates:
- Define geographies based on where the business actually operates or plans to operate
- Do not use generic region buckets (e.g. "Europe") when the plan has specific market activation sequencing — break out priority markets individually and use a "Rest of" bucket for the remainder
- Markets that have not yet been activated must be zero in the periods before activation

Both sections must sum to the same Total in every year. This is a hard requirement.

Add a % Inc. column for every year from the second period onward — formula driven, not hardcoded. Apply conditional formatting consistent with other tabs.

---

## The Bridge Tab

The Bridge tab is the mechanism that connects persona revenue to channel and geography figures. It must be built before the Top Line is populated.

**If a Bridge tab already exists** — review the existing channel and geography breakdowns. Confirm they reflect this client's specific business model. Amend the breakdown structure if needed before setting allocations.

**If no Bridge tab exists** — build it as part of this skill before touching the Top Line.

### Bridge Tab Structure

**Section 1 — Channel Allocation Matrix**
Rows: one per persona × channel combination
Columns: one per year across the plan horizon
Values: % of persona revenue allocated to each channel, per year
Constraint: allocations must sum to 100% per persona per year. Zero where a channel does not exist for that persona in that period.

**Section 2 — Geography Allocation Matrix**
Same structure as channel — one per persona × geography combination, % per year, must sum to 100%.

**Section 3 — Derived Channel Revenue**
Formula-driven: persona revenue (from Customer Objectives) × channel allocation %. Feeds Top Line directly.

**Section 4 — Derived Geography Revenue**
Same structure — formula-driven, feeds Top Line directly.

All Top Line cells must reference Bridge derived rows via formula — never hardcode a Top Line figure.

---

## Build Process

### Phase 1 — Confirm Prerequisites

Before starting:
- Customer Objectives tab is locked and contains confirmed persona revenue figures across the full plan horizon
- Brand Objectives tab is locked
- The client's channel and geography structure is understood

If either objectives tab is not locked, stop and complete it first.

### Phase 2 — Define Channel and Geography Breakdowns

Before building the Bridge, confirm with Michele:
- Which channels does this business actually use today?
- Which channels are planned for the future and in which periods?
- Which geographies are active today?
- Which geographies are planned and in which periods?

This is client-specific. Do not assume a standard breakdown applies. Read all available documents — strategy documents, journey maps, briefs — before asking Michele for input.

### Phase 3 — Build or Amend the Bridge Tab

With channel and geography breakdowns confirmed, build the allocation matrices:

For each persona × channel × year:
- Assign a % allocation based on how that persona actually buys through that channel
- Use the journey maps as the primary source — channel behavior is documented there
- Zero where the channel does not exist for that persona in that period
- Verify each persona's allocations sum to 100% per year before proceeding

For each persona × geography × year:
- Assign a % allocation based on where that persona is located and when geographic expansion activates
- Zero for markets not yet activated
- Verify each persona's allocations sum to 100% per year

Apply the derived revenue formulas: persona revenue (Customer Objectives) × allocation % = derived channel/geo revenue.

### Phase 4 — Establish Current Baseline

For each channel and geography, establish the current baseline:
- Pull from available data sources: sales files, analytics reports, POS data
- Where data exists but is incomplete, triangulate from available proxies (unit quantities × estimated ASP, partial channel data × known share)
- Where no data exists (true startup, new channel), baseline is zero
- Where data should exist but has not been provided, make a reasoned estimate based on available proxies and flag for client confirmation — a working number with a flag is more useful than a blank cell
- TBC is the last resort — only use it when no estimate is possible

### Phase 5 — Verify Reconciliation

Before populating Top Line, verify in the Bridge that:
- Channel derived revenues sum to the Customer Objectives total in every year
- Geography derived revenues sum to the Customer Objectives total in every year
- No channel or geography has a non-zero value in a period where it does not yet exist

Fix allocation assumptions in the Bridge until reconciliation is exact. Do not adjust the Customer Objectives total to force reconciliation — the persona revenue figures are the anchor.

### Phase 6 — Populate Top Line via Formulas

Wire every Top Line cell to the corresponding Bridge derived row via formula. No hardcoded values in the Top Line data cells.

Add % Inc. formulas for all rows from the second period onward.

Apply conditional formatting: green (#E4EDED) when growing, orange (#F7E3DD) when declining, no fill when flat — consistent with Customer Objectives tab.

### Phase 7 — Sense Check

With Top Line populated, verify the story makes sense:
- Do channel trends reflect the strategic sequencing established in Customer Objectives and Big Picture?
- Do declining channels (e.g. fairs being replaced by events/B2B) show a credible transition curve?
- Do geographic activations align with the brand expansion sequencing from the Brand column?
- Is the service revenue trajectory realistic given current capability and Dennis's time?

Flag any figure that cannot be explained by a specific customer behavior assumption.

### Phase 8 — Debrief

Summarize the through-line: what does the Top Line tell us about how the business transforms over the plan horizon? Connect it back to the customer sequencing and brand expectations before moving to the Timeline tab.

---

## Excel Writing Rules

- All Top Line data cells: formula-driven from Bridge, never hardcoded
- All Bridge allocation cells: manual inputs (%), clearly labelled by persona and year
- All Bridge derived revenue cells: formula-driven from Customer Objectives × allocations
- % Inc. cells: formula-driven
- Current baseline: real data where available, reasoned estimate with flag where not, zero for true startups or non-existent channels/markets
- Conditional formatting consistent with Customer Objectives tab
- Add 2031 column if Customer Objectives runs to 2031
- Geography: break out priority markets individually, use "Rest of [region]" bucket for remainder
- Save as new version — never overwrite the source file

---

## Reconciliation Note

The Top Line is the final reconciliation point in the PLAN workbook. Before moving to the Timeline tab, verify that:
- Total business trajectory is consistent across Customer Objectives, Brand Objectives, and Top Line
- Brand metric targets (e.g. B2B inbound leads in Brand Objectives) are consistent with B2B revenue trajectory in Top Line
- No figure in any tab contradicts a figure in another tab

If inconsistencies exist, resolve them before proceeding. The Timeline tab is built on top of a locked, internally consistent plan.
