---
name: customer-objectives
description: Use this skill whenever Michele asks to build or populate the Customer Objectives tab of a PLAN workbook — for any client, any engagement. Triggers on phrases like "let's do customer objectives," "fill in the customer tab," "build the persona targets," or any request to set revenue or lifecycle targets by persona. This is the first planning tab after the Big Picture — always complete it before Brand Objectives or Top Line. Assumes an empty sheet unless told otherwise.
---

# Customer Objectives Tab — Build Process

The Customer Objectives tab translates the strategic persona prioritization into concrete, time-phased revenue targets and lifecycle focus per persona. It is the first planning tab because strategy is customer-led — revenue and brand objectives flow from here, not the other way around.

---

## What It Is Not

- Not a top-down revenue forecast. Never start with a total and divide it out by persona. Build from the bottom up — persona by persona in absolute values — and let the total be an output.
- Not aspirational percentages. Shares are a cross-check, not a starting point.
- Not a marketing plan. Lifecycle focus indicates the strategic emphasis per period, not the tactics behind it.

---

## Tab Structure

Three sections per persona group:

**Share of Business** — each persona's % of total revenue, current through plan horizon. Output of the absolute value model, not an input.

**Total Business** — absolute revenue per persona per year, denominated in €000s. This is the primary planning surface.

**Lifecycle Focus** — strategic emphasis per persona per period:
- **Acquisition** — building the customer base
- **Retention** — keeping and growing existing customers
- **Acquisition + Retention** — both running simultaneously
- **Full Funnel** — acquisition, retention, and reactivation all active; steady state
- **Not a Priority** — persona not yet in focus for this period
- **Transition** — managed decline or handover (e.g. legacy persona being phased out)

Add a YoY growth rate row below the total line — formula-driven, not hardcoded.
Add a Stretch Total row below the base — what is achievable if key assumptions outperform.
Apply conditional formatting: green (#E4EDED) when a figure grows year over year, orange (#F7E3DD) when it declines, no fill when flat.

---

## Build Process

### Phase 1 — Read Everything

Before forming any view, read all available documents:
- Brand and consumer strategy document
- Consumer universe and persona files
- All journey maps for every available persona
- Any existing financial data, sales reports, or analytics

Extract what is already known: current revenue by channel, persona behavior, purchase patterns, channel fit. Do not reconstruct what is already documented.

### Phase 2 — External Research

Research category benchmarks relevant to the client's business model:
- Typical conversion rates, AOV, and growth rates for comparable businesses
- Channel economics (online, B2B, events, fairs) for the relevant category
- Any market sizing that contextualizes the growth assumptions

This grounds the projections. A plan built only on internal logic is not a plan.

### Phase 3 — CEO Briefing

One focused input session before touching the sheet. Resolve:
- What is the current total business size? How is it split today — by channel, by persona, or by product line?
- Which personas are priority in the near term and why?
- Are there known constraints — supply chain lead times, production capacity, resource limits — that cap growth for any persona?
- What does success look like over the plan horizon?

Get this once. Do not extract it piecemeal as you build each persona row.

### Phase 4 — Establish the Baseline

Determine current total business size before modeling forward:
- Use available financial data first
- If incomplete, triangulate from what is known (e.g. one channel's revenue + its known share = total)
- Round to a clean working number — this is a planning baseline, not an audit figure
- Confirm with Michele before proceeding

Split the baseline by persona using current share estimates. These become the Current column in Total Business.

### Phase 5 — Model Forward, Persona by Persona

For each persona, build the absolute value projection year by year based on:
- What changes in their activation — infrastructure built, channels opened, investment made
- Known constraints — supply, capacity, timing — that limit how fast they can grow
- Sequencing logic — not all personas activate at once; earlier-priority personas get the growth investment first
- Channel fit — how each persona buys determines what drives their revenue growth (B2B project relationships vs. site conversion vs. event-based vs. passive halo)

Key rules:
- A persona cannot grow in a period where no investment or change is planned for them
- Retention cannot appear in lifecycle focus until the infrastructure to do retention exists (email list, CRM, contact data)
- B2B-led growth (Luca-type) is constrained by supply chain lead times — production is planned years in advance
- Self-serve online growth (Nadia-type) is constrained by traffic and conversion — model from known site data
- Legacy personas (Marco-type) should hold flat in absolute terms unless there is a specific reason for decline

### Phase 6 — Build the Stretch Model

Once the base model is locked, build a stretch version:
- Identify the 1-2 assumptions most likely to outperform
- Apply those upside assumptions to the relevant personas only
- Do not apply stretch assumptions universally — stretch must be earned by a specific driver
- Stretch total = base total + identified upside, recalculated from persona level up

### Phase 7 — Back-Check Shares

Once absolute values are locked for both base and stretch:
- Calculate shares as outputs — persona absolute / total
- Verify the shares tell a coherent story (priority personas growing share, legacy declining)
- If shares look wrong, interrogate the absolute values, not the shares

### Phase 8 — Set Lifecycle Focus

After absolute values are confirmed, assign lifecycle focus per persona per period:
- Reflect what is actually possible given infrastructure, not just aspiration
- Lifecycle focus must be honest — if retention infrastructure does not exist yet, do not mark Retention
- Every persona eventually reaches Full Funnel — the question is when
- Flag the period when each persona transitions from Not a Priority to active

### Phase 9 — Flag Open Questions

Before presenting, identify any assumption that depends on client-side data not yet available. Log each as a clearly labelled question in the sheet below the data. Do not leave assumptions unexamined — surface the dependency explicitly.

Common open questions:
- Does surplus product exist at end of season? (affects B2B/project growth assumptions)
- What are actual COGS and shipping costs? (affects margin and threshold modeling)
- Are there existing B2B relationships not yet documented?

### Phase 10 — Present Once, Complete

Do not present the sheet until all of the following are resolved:
- Absolute values confirmed for all personas, all years
- Shares verified as outputs
- Lifecycle focus assigned and defensible
- Stretch model complete
- Conditional formatting applied
- Open questions logged in the sheet
- YoY growth rate row formula-driven and verified

Present once. Answer questions. Make surgical updates only.

---

## Reconciliation Note

The Customer Objectives tab is the starting point, not the final word. Once Brand Objectives and Top Line are built, a reconciliation pass checks that:
- Persona revenue targets are consistent with channel revenue targets in Top Line
- Brand investment implied by the objectives is consistent with Brand Objectives
- The total business trajectory is commercially credible

Reconciliation is a separate step — do not attempt it while building this tab.

---

## Excel Writing Rules

- Denominate Total Business in €000s — write 15, not 15,000
- Shares as decimals — write 0.15, not 15%
- YoY growth as formula: =(current year - prior year) / prior year
- Conditional formatting: green (#E4EDED) if cell > prior year cell, orange (#F7E3DD) if cell < prior year cell, no fill if equal
- Text only in Lifecycle Focus cells — no formulas
- Open questions logged as plain text below the data table, clearly labelled
- Save as new version — never overwrite the source file
- No formatting changes beyond what is explicitly requested
