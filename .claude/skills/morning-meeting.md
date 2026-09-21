---
name: morning-meeting
description: Three-phase morning briefing workflow. Phase 1 silently gathers comprehensive data (calendar, inbox with attachments, job search, correspondence, sector news). Phase 2 presents findings interactively. Phase 3 executes batch email cleanup.
tags: [daily, morning, briefing, three-phase]
---

# Morning Meeting: Three-Phase Daily Briefing

Michele's morning meeting operates in three distinct phases, executed in order. Phase 1 runs silently with comprehensive data gathering. Phase 2 presents findings interactively with proactive recommendations. Phase 3 executes batch operations.

## Phase 1: Silent Research & Comprehensive Data Gathering

Execute all research silently without prompting Michele. Gather complete data across five domains before moving to Phase 2.

### 1. Calendar Preparation

Use `morning-calendar-prep` as foundation with these enhancements:

- Fetch today's calendar events
- Filter to "real meetings": exclude personal solo blocks (solo events with only Michele as attendee or Michelle as organizer)
- For each real meeting:
  - Extract attendees (names and count)
  - Pull meeting context from email threads or linked documents
  - Identify any attachments or prep materials referenced
  - Surface time requirements and any pre-meeting actions

**Output structure**: Calendar summary organized by time with prep notes for each meeting.

### 2. Inbox Triage: Comprehensive Sweep with Attachments

Run full inbox-zero sweep with attachment reading capability.

**Setup for attachment reading:**
- Use `mcp__Gmail__get_thread` with parameter `messageFormat: "FULL_CONTENT"` for all emails
- This automatically retrieves attachment metadata AND content in single call
- Extract all attachments inline without separate API calls

**Inbox categories:**
1. **Institutional/Business Emails** (High priority for review):
   - Identify by sender domain or formal structure (e.g., v.pacifico@ied.it, board emails, vendor communications)
   - Read ALL attachments using FULL_CONTENT format
   - Extract: sender org, subject, key content, attachment summaries with action items
   - Special case - PDF institutional docs: extract text, identify structure (headers, body, calls-to-action), summarize with full key instructions
   - Example: Valeria Pacifico IED email contains activation instructions in PDF attachments—extract and present inline with no additional user steps

2. **Messages Requiring Response**:
   - Identify threads where Michele's response is needed
   - Note: exclude emails explicitly waiting on someone else's reply
   - Extract: sender, subject, action required, deadline if any

3. **Mass Emails/Newsletters/Promotions** (flagged for Phase 3 cleanup):
   - Exclude from detailed review
   - Flag for trashing EXCEPT PayPal-related emails
   - Category these for cleanup execution

4. **FYI/Informational**:
   - Messages that don't require response, informational only
   - Summarize if relevant to Michele's business areas

**Exclude from triage**: Personal personal exchanges (use judgment—newsletters and mass emails are not personal exchanges), items already actioned.

**Output**: Organized list by category with full attachment content where applicable.

### 3. Job Search Status

Scan relevant email threads for:
- Active job applications with status
- Deadlines and next steps
- Contact information for current opportunities
- Any recent interviews or follow-ups

Extract current status with actionable next steps.

### 4. Relationship Correspondence

Pull emails from key relationships requiring attention:
- Personal exchanges (not mass emails)
- Messages flagged as important or requiring response
- Vendor/partner communications
- Collaborator coordination

Flag items that need Michele's response.

### 5. Sector News with Substance

Use `morning-sector-news` as foundation with substance layer:

**Gather headlines:**
- Comprehensive newsletter sweep (all newsletters, not just recent)
- Web search across fashion, retail, beauty, luxury sectors
- Dedup multi-source coverage

**Organize into four tiers (present all headlines upfront, then offer drilling):**

**Tier 1: Macro Trends with Business Impact**
- Industry-wide trends (consumer behavior, market shifts, regulatory changes)
- For each: headline + substance (what's happening, why it matters to Michele's sectors, economic/strategic implications)

**Tier 2: Eyewear & Startup News**
- Eyewear industry news
- Relevant startup/innovation coverage
- For each: headline + substance

**Tier 3: Brand/Company Headlines**
- Individual brand moves, launches, personnel changes
- For each: headline + substance (cultural relevance, market position, why it matters)

**Tier 4: Drop (Not included in daily)**
- Unrelated verticals—exclude entirely

**For each headline, include:**
- What's happening (the story)
- Why it matters (business relevance to Michele's focus areas)
- Underlying mechanism (how does it work / what makes it significant)
- Source and full article context available for drilling

Example substance format:
- "AI Supply Chain Optimization (Tier 1)"
  - Story: Multiple luxury retailers deploying AI for inventory prediction
  - Relevance: Directly impacts fashion/retail operations efficiency
  - Mechanism: ML models predict demand patterns, reduce overstock/stockouts, lower acquisition costs
  - Source: [article link] + full context available

### Phase 1 Output Structure

Before moving to Phase 2, compile all findings into organized summary:

```
PHASE 1: COMPREHENSIVE RESEARCH COMPLETE

CALENDAR (Today)
- [Meeting 1 with prep notes]
- [Meeting 2 with prep notes]

INBOX TRIAGE
Institutional/Business Emails:
- [Valeria Pacifico IED email - attachment summary + full activation instructions]
- [Other institutional emails with attachments]

Messages Requiring Response:
- [Listed with sender, subject, action]

Relationship Correspondence:
- [Personal exchanges needing response]

FYI/Informational:
- [Summarized]

Flagged for Phase 3 Cleanup:
- [Newsletter/promotional email count and types]

JOB SEARCH STATUS
- [Current applications with deadlines]

SECTOR NEWS (Four Tiers)
Tier 1 - Macro Trends:
- [All headlines upfront with substance]
Tier 2 - Eyewear/Startup:
- [All headlines upfront with substance]
Tier 3 - Brand Headlines:
- [All headlines upfront with substance]
```

---

## Phase 2: Interactive Walkthrough & Decision Making

Present Phase 1 findings to Michele in structured order. Lead proactively—make recommendations, don't ask for permission constantly.

**Execution order:**
1. Calendar briefing (meetings, prep materials)
2. Inbox triage (institutional emails first, then required responses, then relationships)
3. Job search status
4. Relationship correspondence
5. Sector news (all headlines upfront, then offer drilling by tier)

**For each section:**
- Present findings clearly and decisively
- Offer drill-down capability for detailed context (full article text, attachment details, etc.)
- Make proactive recommendations (e.g., "This institutional email requires immediate IED email activation—here are the steps")
- Only ask for explicit decisions where Michele needs to choose (not permission-seeking)

**Tone:** Lead the meeting as Michele's right hand. Present findings as the expert briefing her, not as a subordinate seeking approval.

---

## Phase 3: Batch Execution

Execute cleanup and any approved actions without repeated permission prompts.

**Email Cleanup:**
1. Identify all newsletters and promotional mass emails from Phase 1
2. **EXCLUDE**: Any PayPal-related emails—preserve these
3. Trash identified newsletters/promotions
4. Use `permission_mode: "dontAsk"` to avoid per-operation permission prompts

**Confirmation:**
- Report completion: "Newsletter cleanup complete. [X] emails trashed, PayPal emails preserved."

---

## Technical Implementation Notes

### Gmail API: Attachment Reading
All Gmail calls use `messageFormat: "FULL_CONTENT"` to automatically include attachments:
```
get_thread:
  threadId: [target thread]
  messageFormat: "FULL_CONTENT"
Response includes: attachments array with {filename, mimeType, content}
```

### Institutional Email Detection
Identify by:
- Sender domain pattern (educational: *.ied.it, *.edu; vendor/partner: recognizable domains)
- Email structure and formality (formal headers, CC lists, official signatures)
- Content signals ("dear faculty," "institutional communication," formal letterhead)

### Permission Mode for Phase 3
Set `permission_mode: "dontAsk"` to eliminate per-operation approval prompts during batch email deletion.

### Newsletter Sources for Comprehensive Sweep
- Gmail search: `subject:(newsletter|digest|weekly|daily) is:unread OR is:read`
- By sender domain (identify known newsletter senders)
- By category (Gmail auto-categories newsletters)
- Search for specific known sources (Vogue Business, WWD, Glossy, etc.)

### News Substance Requirements
Never present headlines alone. Each headline must include:
1. **What**: Description of the story
2. **Why**: Business relevance and impact to Michele's sectors (fashion, retail, beauty, luxury)
3. **How**: Underlying mechanism or context that explains significance
4. **Source**: Link to full article for drilling

---

## Execution Checklist

### Phase 1 Completion
- [ ] Calendar events fetched and filtered (real meetings only)
- [ ] All inbox emails reviewed with FULL_CONTENT format for attachments
- [ ] Institutional emails identified and attachment content extracted inline
- [ ] Valeria Pacifico IED email: both PDFs read, activation instructions extracted
- [ ] Job search status gathered
- [ ] Relationship correspondence identified
- [ ] Comprehensive newsletter sweep (no gaps)
- [ ] Sector news tiered with substance for each headline
- [ ] All findings organized for Phase 2 handoff

### Phase 2 Completion
- [ ] Calendar briefing presented
- [ ] Inbox triage presented (institutional emails first, with full attachment context)
- [ ] Job search status presented
- [ ] Correspondence reviewed
- [ ] Sector news presented (all four tiers with headlines upfront, substance included)
- [ ] Drill-down capability available for detailed context
- [ ] Michele's decisions captured

### Phase 3 Completion
- [ ] Newsletters/promotions identified and ready for cleanup
- [ ] PayPal emails identified and excluded from deletion
- [ ] Batch deletion executed with `dontAsk` permission mode
- [ ] Cleanup completion confirmed

---

## Integration with Existing Skills

This skill orchestrates three existing backend skills as components:
- **morning-calendar-prep**: Base for calendar section (with enhancements)
- **morning-inbox-triage**: Base for inbox section (with attachment reading and institutional email handling)
- **morning-sector-news**: Base for sector news section (with substance extraction layer)

Phase 1 coordinates these plus adds job search and relationship correspondence sections not in individual skills.
