---
name: long-term-operating-strategy
description: Use this skill whenever Michele asks to write or update the Long-Term Operating Strategy document for a client engagement. Triggers on phrases like "write the LTOS," "build the operating strategy," "draft the long-term strategy document," or any request to produce the strategic narrative document that sits above the Annual Operating Plan. Always complete the PLAN workbook (Big Picture, Customer Objectives, Brand Objectives, Top Line, Timeline) before writing this document — it synthesizes those tabs into prose. Output is a .docx file.
---

# Long-Term Operating Strategy — Writing Process

The Long-Term Operating Strategy (LTOS) translates the Constitution, Manifestos, and PLAN workbook into a strategic narrative. Where the foundational documents are permanent, the LTOS is situational and time-bound. It covers the full plan horizon directionally and is updated at each annual planning cycle. It is not an action plan. It does not contain "this year" operational detail — that lives in the Annual Operating Plan, a separate document produced each year.

The LTOS serves three audiences simultaneously: the consulting team, the client and founder, and the stakeholders the client will share it with (board, shareholders, employees). It must work for all three without being rewritten for each.

---

## What It Is Not

- Not an action plan or task list
- Not a "this year" operational document — that is the Annual Operating Plan
- Not a client-specific template — the structure is universal across all engagements
- Not a marketing document — it is a strategic document written for a board-level audience

---

## Document Structure

Every LTOS follows this structure, in this order:

1. **Title block** — client name, document name, date
2. **About This Document** — what it is, what it covers, its relationship to other documents (Constitution, Manifestos, Annual Operating Plan), and its intended audiences
3. **Situation** — where things stand today. Two sub-sections always present: The Market and The Business. Data-led where data exists; narrative where it does not.
4. **Complication** — what makes the current situation insufficient or unsustainable. The tension that makes strategic action necessary.
5. **Stakes** — why now. What is at risk if nothing changes. Brief — two paragraphs maximum.
6. **Vision** — where the business is going. The destination, stated plainly. Not a mission statement.
7. **Objectives** — what must be achieved in sequence to reach the vision. Three objectives in sequence is the right number for most engagements. Each is a genuine milestone, not a step.
8. **Strategy** — how. Three components in order: framing paragraphs (the overall logic), the timeline table, phase-by-phase prose.

---

## Build Process

### Phase 1 — Read Everything

Before writing a single word, read:

- The bundled reference example at `references/example-ltos.md` to calibrate register — this step is mandatory, not optional. It is illustrative and generic, not a real client, never substitute a specific client's document here even if one is available in chat; a real client's LTOS is that client's confidential content and doesn't belong referenced inside a skill every other client's engagement also runs on
- All completed PLAN workbook tabs: Big Picture (Situation/Complication/Expectation/Requirement per column), Customer Objectives, Brand Objectives, Top Line, Timeline
- The existing brand strategy document if one exists — it may contain prose that can be elevated rather than reconstructed
- All analytics reports, sales data, and research gathered during the engagement
- The Constitution and Manifestos for foundational language

The LTOS synthesizes all of this. Nothing in the document should be invented — every claim must trace back to a source document, a data point, or a confirmed client statement.

### Phase 2 — Calibrate the Tone

Before drafting, determine where this engagement sits on the data-to-narrative spectrum:

- **Data-rich engagement** (established business, analytics available, market research conducted): lean analytical. Lead with figures, cite sources, use market data to anchor claims.
- **Data-thin engagement** (startup, pre-revenue, limited research): lean narrative. The emotional and strategic logic carries more weight. Figures are used sparingly and only when confident.

Most engagements sit somewhere between the two. The tone should reflect the evidence available — never overclaim precision when data is thin, never undersell with vague language when hard numbers exist.

### Phase 3 — Draft Situation

**The Market sub-section** answers: what is happening in the external environment that makes this moment significant? Consumer trends, market dynamics, competitive landscape, regulatory context. Always grounded in real data where available. Cite figures from live research only — never training-data statistics.

**The Business sub-section** answers: where does this business actually stand today? Be honest — including about what is undeveloped, undocumented, or not yet working. The Situation is not promotional. It is a clear-eyed account of the current state.

### Phase 4 — Draft Complication

The Complication names the tension — what makes the current situation insufficient or unsustainable. It flows directly from the Big Picture tab's Complication row, elevated into prose.

Two or three sub-sections, each addressing a different dimension of the complication (e.g. The Brand Is Invisible / The Model Is Not Scalable). Each sub-section is two to three paragraphs. The complication should be honest without being catastrophizing — it names the real tension, not a list of everything that could go wrong.

### Phase 5 — Draft Stakes

Two paragraphs maximum. The first: why now — what is time-sensitive about the opportunity or the risk. The second: what is at stake if the business does not act — what gets harder, what closes off, what gets claimed by someone else. Brief, direct, no dramatization.

### Phase 6 — Draft Vision

One to two paragraphs. Plain language — what the business looks like at the end of the plan horizon. Include: the brand's position in the market, the revenue scale, the geographic footprint, the founder's role, the operational state. Not a mission statement. Not aspirational language divorced from the numbers.

### Phase 7 — Draft Objectives

Three objectives, stated in sequence. Each is a genuine milestone — not a step, not a phase. Each must be actually achieved before the next is pursued. Written as prose, not as a numbered list. The connection between objectives should be explicit: what does achieving the first one unlock for the second?

### Phase 8 — Draft Strategy

**Framing paragraphs first.** Two to three paragraphs explaining the overall strategic logic: what the business is doing and why, in what order, driven by what sequencing principle. Customer sequencing and geographic sequencing should both be addressed if relevant.

**Timeline table second.** A simplified version of the PLAN workbook Timeline tab — three rows only:
- Period (columns for each timeframe)
- Theme (one short phrase per period)
- State (one to two sentence summary of the company's overall state in that period)

Do not reproduce the full node-by-node Timeline. The detail lives in the PLAN workbook. The table in the LTOS is the board-level summary only.

**Phase prose third.** One sub-section per phase, named by theme (e.g. "Foundation (Q1–Q3 2026)"). Two to three sentences per phase — the directional flavor of that period, not an operational plan. Each should feel like a natural continuation of the table row above it.

---

## Writing Rules

**No em dashes.** Use a comma, a colon, or a new sentence instead.

**No contractions.** The document is formal.

**No task language.** The document describes strategic states and outcomes, not activities. "The brand is present in relevant circles" not "build brand presence in relevant circles."

**No bullet points in the body.** The document is prose throughout, except for the timeline table.

**Figures must be sourced.** Every statistic must come from a document or live research conducted during the engagement. Never use training-data figures. If a figure cannot be sourced, state it as an estimate and flag it.

**Short paragraphs.** Two to four sentences each. The document should be readable at board pace, not academic pace.

**Four to six pages maximum.** Tight is better. The Annual Operating Plan carries the detail.

---

## Building the .docx

Use the docx npm library. Follow the SKILL.md for docx creation.

Document formatting:
- Font: Calibri throughout
- Body text: 11pt (size: 22 in DXA)
- H1 (section headings): 14pt bold
- H2 (sub-section headings): 12pt bold
- Spacing: 160 after body paragraphs, 400 before H1, 280 before H2
- No color, no decorative elements — clean and boardroom-ready
- Page size: A4

Timeline table:
- Three rows: Period, Theme, State
- Header row lightly shaded (D9D9D9)
- All columns equal width except the label column (slightly wider)
- Wrap text in all cells
- No aggressive borders — standard thin borders only

After building, render to PDF and view every page before presenting. Verify:
- Table renders correctly and does not clip
- No orphaned headings at the bottom of a page
- Em dashes did not slip through
- All figures are accurate

---

## Relationship to Other Documents

**Constitution and Manifestos** — permanent, never change. The LTOS references them but does not reproduce them.

**PLAN Workbook** — the living numbers layer. The LTOS synthesizes the narrative from it but does not reproduce the tables. The reader is directed to the PLAN workbook for the detailed figures.

**Annual Operating Plan** — the operational detail for the current year, produced each year. For smaller clients, the roadmap serves this function. For larger or more structured clients, a full planning file and rolling operating forecast.

**The LTOS is updated annually** at planning time — not replaced. The Situation and Complication sections are updated to reflect what changed. The Vision and Objectives evolve as milestones are reached. The Strategy section's timeline table rolls forward by one year each cycle.
