# Field Kit to Repo Mapping

*Where field kit outputs go back into the formal repo workflow.*

*Source: adapted from `IMPLEMENTATION_PLANNING/CAMPAIGN_BRIEF_WORKFLOW_DISCOVERY_v0.1.md` and `IMPLEMENTATION_PLANNING/FIRST_IMPLEMENTATION_SLICE_PLAN_v0.2.md`.*

---

## Mapping Table

| Field Kit Output | Repo Destination | When |
|---|---|---|
| Campaign discussed | `CAMPAIGN_BRIEF_WORKFLOW_DISCOVERY_v0.1.md`, Section 2 (Selected Workflow) | After first conversation |
| Workflow start/end, cadence | Category 1 output table (Workflow Boundary) | After first conversation |
| Requester / Domain Expert / Governance Owner | Category 1 output table (roles) | After first conversation |
| Brief fields (required, optional, generated) | Category 2 output table (Campaign Brief Structure) | After first conversation |
| Information sources checked | Category 3 output table (KB / Information Surfaces) | After first conversation |
| Authority levels (binding/advisory/background/anecdotal) | Information Surface Registry draft (Section 6 of discovery worksheet) | After first conversation |
| Claims and governance notes | Later Category 6 discovery (Policy / Governance Boundaries) | Second discovery pass |
| Assumptions and confidence | Later Category 5 discovery (Assumptions / Premises) | Second discovery pass |
| Sufficiency notes | Later Category 7 discovery (Sufficiency / Stopping) | Second discovery pass |
| Outcome signal and timing | Slice Plan / Outcome Record design | After first conversation |
| Learning notes (lessons, what carried forward) | Later Learning Event / MUO design (Category 9) | Second discovery pass |
| Prototype opportunity / reasoning that disappears | Slice Plan — validation of workflow selection | After first conversation |
| Things the prototype should NOT do | Slice Plan — exclusions / constraints | After first conversation |
| Artifacts/documents requested | Information Surface Registry — new surfaces to register | After first conversation |

---

## Workflow

```text
Stakeholder conversation
        |
        v
Notes Capture Template (05_NOTES_CAPTURE_TEMPLATE.md)
        |
        v
Campaign Brief Workflow Discovery worksheet
(IMPLEMENTATION_PLANNING/CAMPAIGN_BRIEF_WORKFLOW_DISCOVERY_v0.1.md)
        |
        v
Fill Category 1-3 output tables
        |
        v
Data model sketch (next step — not yet created)
        |
        v
Build backlog (later — not yet created)
```

---

## Warning

Do not convert notes directly into schema or backlog until the discovery worksheet (Categories 1-3) is filled and reviewed.

Notes are raw discovery. The worksheet structures them into build inputs. The schema translates build inputs into data objects. The backlog sequences the build. Each step depends on the previous step.
