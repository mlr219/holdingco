# Holding Co. — Org Chart

This repo is the cross-entity coordination layer: Cross-entity, Holding Co., per the group structure. It sits above MLR Global, Martini Pomanti, and Me, not inside any of them.

## Built and live in this repo

1. **Chief of Staff** (`chief-of-staff`) — holds and tracks account roadmaps handed up from account managers, across every entity. Reports to the CEO.
2. **CSO** (`cso`) — canonical source for the cross-client Chief Strategy Officer persona. Working copies live in each client repo that needs it (currently `dennisbotaniccollection`); this is the version to update when the role changes, then propagate the copy. Governed by `senior-leadership-standard.md`.
3. **Senior Leadership Standard** (`senior-leadership-standard.md`) — universal base layer for every C-suite persona (CSO, CMO, CCO, CXO, COO, Chief of Staff). Canonical source here; duplicated into client repos that use it (currently `dennisbotaniccollection`).
4. **LTOS skill set** — six skills (`big-picture`, `customer-objectives`, `brand-objectives`, `top-line`, `timeline`, `long-term-operating-strategy`) for building a client's PLAN workbook and Long-Term Operating Strategy document. Canonical source here, but these run at account level via packaged `.skill` installs, not per-repo. See `SOURCES.md`.

## CEO

Michele. Not a persona — she is the CEO, not something this repo automates.

## Documented for later, not built yet

Chief of Staff's fuller mandate: capacity budgeting per entity, a single cross-entity calendar, reallocation on a set cadence, and the escalation path when an entity needs more than its allocation. See `chief-of-staff.md` for detail. Build these only when there's real cross-entity capacity conflict to arbitrate, i.e. once a second entity or business unit is genuinely competing with Dennis Botanic Collection (or whatever comes next) for time.

## Entities reporting in

- **MLR Global** — consulting (MLRCC), teaching, publishing, concepts, corporate/admin. Dennis Botanic Collection is MLRCC's first client, under the Mom&Pop segment (not yet built as its own repo).
- **Martini Pomanti** — vineyard, hospitality, food.
- **Me** — Michele's personal and professional brand plus life admin.

Each entity gets its own repo when there's real work to put in it, not before.
