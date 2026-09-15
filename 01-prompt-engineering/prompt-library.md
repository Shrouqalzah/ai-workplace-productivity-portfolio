# Prompt Library

This library contains reusable prompts for recurring Business Analyst tasks on the GovConnect scenario. Each prompt follows either the C.A.R.E. framework (Context, Action, Role, Expected Output) or the R.C.T.O. framework (Role, Context, Task, Output).

| Prompt Name | Workplace Task | Framework | Prompt | Expected Output |
|---|---|---|---|---|
| Requirements Extractor | Turn workshop notes into structured requirements | C.A.R.E. | **Context:** I am a Business Analyst on the GovConnect team reviewing anonymized notes from a stakeholder requirements workshop for a new citizen service-request feature. **Action:** Extract functional requirements, non-functional requirements, constraints, assumptions, open questions, and decisions already made. **Role:** Act as an experienced business analyst supporting a government digital-services team. **Expected Output:** A Markdown table — ID, Category, Statement, Source Evidence, Owner, Status. Use `[Not Specified]` for missing owners. | A traceable requirements table with gaps clearly flagged. |
| User Story & Acceptance Criteria Drafter | Draft a user story from a feature request | R.C.T.O. | **Role:** Act as a Business Analyst drafting user stories for a government citizen-services portal. **Context:** I will provide a short description of a feature request from a department stakeholder. **Task:** Draft one user story (As a / I want / So that) plus 3–5 acceptance criteria in Given/When/Then format. Flag ambiguity needing clarification. **Output:** User story + criteria + an "Open Questions" list. Do not invent functionality not mentioned in the request. | A testable story with flagged clarification points. |
| Meeting Notes → Decision-Ready Brief | Summarize a status/sprint meeting | C.A.R.E. | **Context:** The following are raw notes from a GovConnect status meeting involving the BA, department stakeholders, and the delivery team. **Action:** Create a concise decision-ready brief for the project sponsor. **Role:** Act as a Business Analyst preparing a status brief. **Expected Output:** 3-bullet bottom line first, then Decisions, Risks/Open Questions, and an action-item table (Action Item, Owner, Deadline, Priority, Status). Preserve names/dates/numbers exactly; don't convert open questions into decisions; mark gaps `[Not Specified]`. | A sponsor-ready brief with no invented details. |
| UAT Test Case Builder | Draft UAT test cases from acceptance criteria | R.C.T.O. | **Role:** Act as a Business Analyst preparing User Acceptance Testing materials. **Context:** I will provide one user story with its acceptance criteria for a GovConnect feature. **Task:** Draft UAT test cases covering the happy path, one edge case, and one negative/error case. **Output:** Table — Test Case ID, Scenario, Steps, Expected Result, Pass/Fail (blank), Notes. Base cases only on the criteria provided; don't assume undescribed UI details. | A structured UAT script ready for a department tester. |
| Stakeholder Delay Update Email | Communicate a confirmed schedule change | C.A.R.E. | **Context:** A GovConnect feature release has slipped from an original date to a new date due to a confirmed technical/dependency issue. **Action:** Write a professional email informing affected department stakeholders of the schedule change. **Role:** Act as a Business Analyst communicating on behalf of the project team. **Expected Output:** Subject line + a concise email (~120–160 words) stating old date, new date, and reason plainly, without over-apologizing. Don't speculate about unconfirmed impacts. | A clear, factual update email. |
| Release Planning Assistant | Build a rollout plan for a new feature | C.A.R.E. | **Context:** The GovConnect team needs a plan to roll out a new feature over a defined period. **Action:** Break the rollout into Mechanisms, Phases, and specific Tasks; note dependencies and open decisions. **Role:** Act as a Business Analyst supporting release planning. **Expected Output:** Goal statement, success measure, a phase table (Phase, Objective, Key Tasks, Dependencies), and a short list of open decisions. Don't invent owners/dates not supplied. | A concise Goal→Mechanisms→Phases→Tasks plan. |

## When I Would Use These Prompts
- **Requirements Extractor:** right after a requirements workshop.
- **User Story & Acceptance Criteria Drafter:** once a feature request is agreed in principle, before UAT planning.
- **Meeting Notes → Decision-Ready Brief:** after any working meeting with scattered updates.
- **UAT Test Case Builder:** before a UAT session, to give department testers a structured script.
- **Stakeholder Delay Update Email:** whenever a confirmed timeline change needs communicating to non-technical stakeholders.
- **Release Planning Assistant:** when translating an approved feature into an actionable rollout plan.

## Short Example Outputs

### Example 1 — Meeting Notes → Decision-Ready Brief
- Citizen-facing status tracker confirmed for pilot launch with 3 departments; go-live date `[Not Specified]`.
- Notification integration still pending; deadline `[Not Specified]`.
- UAT ownership for the permits module has not been assigned.

### Example 2 — Stakeholder Delay Update Email

**Subject:** Service Request Tracker — Launch Date Update

Dear Team,

The launch date for the Service Request Tracker has moved from [original date] to [new date], due to a delay in a third-party verification dependency currently being resolved by the technical team.

Please review your own timelines for anything that may be affected, and raise any concerns through the project channel.

Best regards,
Shrouq Alzahrani
Business Analyst — GovConnect

### Example 3 — User Story & Acceptance Criteria Drafter

**Story:** As a citizen applying for a permit, I want to see my application's real-time status, so I don't need to call the department for updates.

**Given/When/Then:** Given an active application, When the citizen logs in, Then they see the current status (Submitted/In Review/Approved/Rejected).

**Open Questions:** What's the required status-update refresh SLA? Should citizens be notified proactively, or only see it on login?
