# Document House Style

Applies to every client deliverable docx (Constitution, Manifestos, PLAN workbook narrative documents, LTOS, and anything else produced as an actual client deliverable). Not for promotional items or proposals, those are pre-client or generic and don't carry this branding.

Extracted directly from a real reference file (`03_DBC_LTOS.docx`, September 2026) and verified against its raw XML. Not guessed.

## Fonts

- Body and headings: **Victory Neue** (headings use it bold, not a separate typeface)
- Theme's defined heading font is "Victory Bold," but the actual heading styles override to Victory Neue plus a bold flag. Follow what the styles actually do, not the theme's nominal major font.
- Both are custom fonts, not shipped with Word. **Open item**: font files for embedding, or an agreed fallback if a reader's machine doesn't have them installed, not yet provided. Until resolved, documents reference the fonts by name only, and will silently substitute on a machine that doesn't have them.

## Sizes

- Body text: 9pt
- Heading 1: 12pt, bold
- Heading 2: 10pt, bold
- Headings in black (`#000000`), not the body's default color

## Color palette (theme-defined)

- Charcoal: `#414141`
- Near-white: `#F9F9F9`
- Medium gray: `#C6C5C4`
- Light gray: `#F2F0F0`
- Terracotta accent: `#D57655`
- Sage accent: `#7AA4A3`

## Header

Two lines, top of every page:
1. **Phase label**, bold, black. Marks which phase of the engagement framework this document belongs to (e.g. "DESIGN"), not the document's type. Only one phase confirmed so far, more to come once Michele finalizes the full document list mapping phase to document to header/footer details.
2. A thin horizontal rule in medium gray (`#C6C5C4`), then the document title (e.g. "Long Term Operating Strategy.") in the same gray, same line or directly below the rule.

## Footer

Right-aligned, bottom of every page:
1. Logo (`assets/mlrcc-logo.jpg` in this repo), positioned bottom-right.
2. Client name, bold, gray (`#B3B3B3`). **Present only once the document is an actual deliverable for a specific, confirmed client** — not while it's a promotional item or a proposal (pre-engagement, generic, unpersonalized).
3. Page number, same gray, not bold.

## Page setup

- A4
- 1-inch (1440 twip) margins on all sides

## Open items

- Font files or fallback for Victory Neue / Victory Bold.
- Full phase list and which document types belong to each phase (Michele is building this out; "Design" is the only confirmed phase today).
- Exact trigger mechanism for the footer's client-name personalization (confirmed conceptually, tied to actual client status, not yet tied to a specific system field or status flag).
