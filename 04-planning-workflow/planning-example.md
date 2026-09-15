# Planning Workflow Example

## Goal
Complete UAT and roll out the Service Request Tracker feature to all GovConnect departments within 6 weeks of receiving a "go" decision, with a phased rollout rather than a single simultaneous launch.

*(Starting facts, carried over from the Information Workflow: UAT is in progress; two critical status-filtering bugs are open; the go/no-go decision is pending from the sponsor; accessibility-review ownership and license-renewal scope are still undecided.)*

## Success Measures
- Both critical UAT bugs are resolved and re-tested before go-live.
- Each department completes onboarding with no unresolved high-priority issues.
- The accessibility review is completed and signed off before the first department goes live.
- Adoption and issue data are reviewed after each phase before the next department is onboarded.

## Mechanisms
*(Proposed — pending sponsor review)*
1. **UAT closure:** resolve open bugs and outstanding test items before any go-live.
2. **Phased onboarding:** roll out department-by-department rather than all at once, to contain risk.
3. **Stakeholder communication:** send a short update after each phase (reusing the Stakeholder Delay Update Email format as the template).
4. **Feedback loop:** collect issues/usage data after each department launch to inform the next phase.

## Phases and Tasks
*(Proposed plan — task breakdown and sequencing require sponsor approval)*

| Phase | Purpose | Actionable Tasks | Main Output |
|---|---|---|---|
| 1. Close out UAT | Resolve blockers before any launch | Fix and re-test the two status-filtering bugs; refresh permit module test data; confirm an owner for the accessibility review; obtain sponsor go/no-go decision | Signed-off UAT and a recorded go decision |
| 2. Pilot with Finance | Validate the feature with the department that already confirmed testing readiness | Schedule pilot start date; prepare short user guidance; monitor issues for one week; collect Finance's feedback | Pilot results and an initial issue log |
| 3. Phased rollout to remaining departments | Extend rollout while managing risk | Sequence remaining departments; send a rollout-schedule update to each; onboard one department at a time; track adoption and open issues per department | Fully onboarded departments with a running issue log |
| 4. Post-launch review | Capture lessons and resolve remaining open items | Review adoption and issue data across all phases; document lessons learned; bring the license-renewal scope question back to the sponsor for a decision | Post-launch review report |

## Dependencies and Open Decisions
- The go/no-go decision from the UAT phase must be resolved before Phase 1 can close.
- Accessibility-review ownership (open since the Information Workflow) must be assigned before Phase 2 begins.
- The license-renewal scope question (open since the Information Workflow) is deliberately deferred to Phase 4 rather than decided here — it does not block rollout of the current scope.
- Department sequencing in Phase 3 is a proposed order, not yet confirmed by the sponsor.
