# Sources

Log of what's in this repo, where it came from, and when it was loaded. Files here are duplicated from the original upload, not live-linked, update this log and the file itself when a source changes.

| File | Source | Loaded |
|------|--------|--------|
| `.claude/skills/big-picture/SKILL.md` | `LTOS_01_Big_Picture.md` (uploaded in chat) | 2026-09-18 |
| `.claude/skills/customer-objectives/SKILL.md` | `LTOS_02_Customer_Objectives.md` (uploaded in chat) | 2026-09-18 |
| `.claude/skills/brand-objectives/SKILL.md` | `LTOS_03_Brand_Objectives.md` (uploaded in chat) | 2026-09-18 |
| `.claude/skills/top-line/SKILL.md` | `LTOS_04_Top_Line.md` (uploaded in chat) | 2026-09-18 |
| `.claude/skills/timeline/SKILL.md` | `LTOS_05_Vision_Timeline.md` (uploaded in chat) | 2026-09-18 |
| `.claude/skills/long-term-operating-strategy/SKILL.md` | `LTOS_06_Document.md` (uploaded in chat) — **amended**: Phase 1 originally hardcoded two real clients' LTOS documents (SAG, Martini Pomanti) by name as a required reference. Fixed to point at a bundled generic example instead, see next row | 2026-09-18 |
| `.claude/skills/long-term-operating-strategy/references/example-ltos.md` | Written in-session: a fictional example (Meridian Coffee Roasters) built to calibrate register without referencing any real client's content | 2026-09-18 |
| `.claude/agents/cso.md` | `CSO_Persona.md` (uploaded in chat) | 2026-09-18 |

These six skills are packaged and installed at the account level (see `.skill` files delivered in chat), not loaded per-repo. This file is the canonical source and version history; the account-level install is what actually runs.

`cso.md` is a persona (agent), not a skill — no account-level install exists for agents. It's duplicated by hand into client repos that need it (currently `dennisbotaniccollection`); this copy is the one to edit when the role changes.

| `templates/Discovery_Workbook_Template.xlsx` | Built in-session from four real discovery worksheets (`W01_Product_Discovery.docx`, `W02_Brand_Discovery.docx`, `W03_Organization_Discovery.docx`, `W04_Consumer_Discovery.docx`, uploaded in chat). Question sets and instructions only — the source files were filled in with SAG's actual answers, which are not reproduced here, same confidentiality principle as the LTOS reference example. | 2026-09-18 |

**Note on placement**: `document-house-style.md`, `cso.md`, `senior-leadership-standard.md`, the six LTOS skills, and `templates/Discovery_Workbook_Template.xlsx` are all MLRCC-specific (Michele's consulting practice), not genuinely cross-entity. They're staying in `holdingco` temporarily until the `mlrcc` repo exists, at which point they move down a level. Only `chief-of-staff.md` and `roadmaps/` are actually Holding Co.-level.
