# Information Processing Example

## Information Tasks Used
This example demonstrates **summarizing, extracting, restructuring, and prioritizing**. A Business Analyst regularly needs to turn scattered UAT/status meeting notes into a brief the project sponsor can act on.

## 1. Raw Input

> UAT session for the Service Request Tracker happened today. Finance department confirmed they can start testing Wednesday. IT flagged that the test environment still needs the permit module data refreshed — not done yet. Ops team asked if the tracker will also cover license renewals — no decision made yet. Two critical bugs found in status filtering; dev team already working on a fix. Sponsor wants a go/no-go decision by end of week. Accessibility review still pending, owner not confirmed. Next sync scheduled for Monday.

## 2. Prompt Used

*(Reusing the Meeting Notes → Decision-Ready Brief prompt from Section 1, applied to the notes above.)*

**Context:** The following are raw notes from a GovConnect UAT status meeting. **Action:** Create a concise decision-ready brief for the project sponsor. **Role:** Act as a Business Analyst preparing a status brief. **Expected Output:** 3-bullet bottom line first, then Decisions, Risks/Open Questions, and an action-item table (Action Item, Owner, Deadline, Priority, Status). Preserve names/dates/numbers exactly; don't convert open questions into decisions; mark gaps `[Not Specified]`.

## 3. AI Output — First Draft

### Bottom Line
- UAT for the Service Request Tracker is underway; Finance begins testing Wednesday.
- The tracker will be expanded to cover license renewals.
- Accessibility review is assigned and in progress.

### Actions
| Action Item | Owner | Deadline | Priority | Status |
|---|---|---|---|---|
| Refresh permit module test data | IT | Wednesday | High | Done |
| Fix status-filtering bugs | Dev team | End of week | High | In progress |
| Complete accessibility review | QA | Monday | Medium | In progress |

## 4. Human Review

The first draft contains unsupported assumptions:
- The source never decided to expand scope to license renewals — Ops only asked; this was incorrectly stated as confirmed.
- The permit module data refresh was marked "Done," but the source says it's not done yet.
- The accessibility review was given an owner ("QA") and a deadline ("Monday") — neither appears in the source; the owner is explicitly unconfirmed.
- "Monday" in the source refers to the next sync, not the accessibility deadline — the draft conflated these.
- The go/no-go decision the sponsor is waiting on was dropped entirely from the first draft.

I corrected these and preserved uncertainty in the final output.

## 5. Final Structured Output

### Bottom Line
- Finance confirmed UAT testing starts Wednesday; the permit module test data still needs refreshing beforehand.
- Two critical status-filtering bugs were found and are being fixed; a go/no-go decision is due from the sponsor by end of week.
- License-renewal scope and accessibility-review ownership remain open.

### Confirmed Decisions
| Decision | Evidence | Status |
|---|---|---|
| Finance begins UAT testing Wednesday | Confirmed by Finance in meeting | Confirmed |

### Action Items
| Action Item | Owner | Deadline | Priority | Status |
|---|---|---|---|---|
| Refresh permit module test data | IT | `[Not Specified]` | High | Open |
| Fix status-filtering bugs | Dev team | `[Not Specified]` | High | In progress |
| Provide go/no-go decision | Sponsor | End of week | High | Pending |
| Complete accessibility review | `[Not Specified]` | `[Not Specified]` | High | Open |
| Decide on license-renewal scope | `[Not Specified]` | `[Not Specified]` | Medium | Open decision |
| Next sync | Project team | Monday | Medium | Scheduled |

*Note: the priority on "Complete accessibility review" was corrected from Medium to High during the Section 5 verification pass, after Section 4's rollout plan established it as a blocker for the pilot phase.*

### Risks and Open Questions
- **Launch-readiness risk:** permit module test data not yet refreshed; UAT could be blocked.
- **Ownership gap:** accessibility review has no confirmed owner.
- **Open decision:** will license renewals be added to tracker scope?
- **Time pressure:** sponsor's go/no-go decision is due end of week, same week as two open critical bugs.
