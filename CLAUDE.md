# Claude Development Notes — Perceived Topography Framework

## Repository Purpose
This is a **theory-building repository**, not a paper-writing project. The paper is one output of the theory.

## Priority Hierarchy
1. **`01_CONCEPT_ARCHITECTURE/`** — The most important folder. Everything else exists to support or challenge it.
2. **`04_FAULT_LINES/`** — Where breakthroughs come from. Systematically preserved contradictions.
3. **`05_EMERGING_CONCEPTS/EC_003_Agentic_Retrieval_and_State.md`** — Watch file. Strong intuition that retrieval explains how perception is constructed. Could become foundational.

## Core Protocol: Conflict Resolution
If a discovery conflicts with the concept architecture:
- **Do NOT change the paper.**
- **Do NOT change the discovery.**
- **Open a fault line in `04_FAULT_LINES/`.**

## Core Protocol: Classification-First
Every new insight MUST be classified before being added:
1. Discovery — A new observation or finding → `02_DISCOVERY_LOG/`
2. Aha Moment — A conceptual breakthrough or reframe → `03_AHA_MOMENTS/`
3. Fault Line — A contradiction or unresolved tension → `04_FAULT_LINES/`
4. Emerging Concept — A nascent idea needing development → `05_EMERGING_CONCEPTS/`
5. Definition Change — A refinement to core terminology → update `01_CONCEPT_ARCHITECTURE/DEFINITIONS.md`
6. Counterargument — A challenge to the framework → `06_COUNTERARGUMENTS/`

Only after classification should the insight be placed.

## Core Protocol: Nothing Becomes Doctrine Alone
No single insight — no matter how brilliant — changes the concept architecture by itself.

Architecture changes **only** when:
1. **Multiple discoveries converge** toward the same revision.
2. **A fault line is resolved** through sustained analysis.

This exists because the strongest repositories eventually become victims of their newest insight. The latest idea feels brilliant and suddenly everything gets rewritten. This protocol resists that.

A discovery does not change architecture. An aha moment does not change architecture. A paper draft does not change architecture. Only convergence or resolution does.

## Session Protocol: Architectural Pressure Report
Every session begins by reading and updating `00_ADMIN/ARCHITECTURAL_PRESSURE_REPORT.md`. This answers:
- What changed since last session?
- What is under pressure?
- What has converged?
- What remains unresolved?

This prevents wandering and keeps research focused on the highest-value questions.

## Session Handoff System (Claude ↔ ChatGPT Workflow)

The OpenAI co-author does not have persistent GitHub access. Claude maintains the repo and generates a clean perception surface for each session.

### Workflow
1. **Before session:** Claude regenerates `00_ADMIN/SESSION_START.md` from CURRENT_STATE.md and ARCHITECTURAL_PRESSURE_REPORT.md. Benet pastes it into ChatGPT.
2. **During session:** ChatGPT works from that state. When filing is needed, co-author says **"Repository Action Required"** and describes classification + content.
3. **After session:** Co-author produces a handoff note. Benet gives it to Claude. Claude files it into `00_ADMIN/SESSION_LOG/SESSION_YYYY-MM-DD.md`, updates the repo, and regenerates SESSION_START.md for the next session.

### Key Files
- `00_ADMIN/SESSION_START.md` — Paste into ChatGPT at session start. Short, self-contained.
- `00_ADMIN/SESSION_HANDOFF_TEMPLATE.md` — Template for end-of-session handoff notes.
- `00_ADMIN/SESSION_LOG/SESSION_YYYY-MM-DD.md` — Archived session handoffs.

### Regeneration Checklist (for Claude)
When regenerating SESSION_START.md:
1. Read CURRENT_STATE.md — update the architecture summary
2. Read ARCHITECTURAL_PRESSURE_REPORT.md — update the pressure areas
3. Count current items (discoveries, fault lines, etc.) — update the counts
4. Check which fault lines and emerging concepts are most active — update the reading order
5. Leave "Current Session Goal" blank for human to fill in

## CURRENT_STATE.md
`01_CONCEPT_ARCHITECTURE/CURRENT_STATE.md` is the "living constitution" — the canonical snapshot of what the framework currently believes. Not history, not evolution, not discussion. Just: if someone joined the project today, what do we currently believe? This file is regenerated with every significant architecture update.

## Folder README Maintenance
Each folder has a `README.md` that lists its contents. When adding or removing files from any folder, update that folder's README to reflect the change.

## Naming Conventions
- Discoveries: `DISCOVERY_NNN_Short_Description.md`
- Aha Moments: `AHA_NNN_Short_Description.md`
- Fault Lines: `FL_NNN_Short_Description.md`
- Emerging Concepts: `EC_NNN_Short_Description.md`
- Counterarguments: `CA_NNN_Short_Description.md`
- Paper Drafts: `PAPER_vX.Y.md`
