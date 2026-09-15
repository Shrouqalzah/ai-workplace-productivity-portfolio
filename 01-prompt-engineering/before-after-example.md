# Before/After Example

## Before (Weak Prompt)
"Write user stories for the new feature."

## Initial Result
A generic, ungrounded story — no named persona, no specific feature, no acceptance criteria. Could apply to almost any system.

## After (C.A.R.E./R.C.T.O. Version)
The **User Story & Acceptance Criteria Drafter** prompt from the Prompt Library, with the specific input:

> "Department stakeholders requested a feature allowing citizens to track the real-time status of their permit application online instead of calling the department."

## Improved Result

**Story:** As a citizen applying for a permit, I want to see my application's real-time status, so I don't need to call the department for updates.

**Given/When/Then:** Given an active application, When the citizen logs in, Then they see the current status (Submitted/In Review/Approved/Rejected).

**Open Questions:** What's the required status-update refresh SLA? Should citizens be notified proactively, or only see it on login?

## What Improved?
- The weak prompt supplied no persona or feature, so the model had to guess; the improved prompt named both explicitly.
- Output moved from an ungrounded story to testable, developer/UAT-ready criteria.
- Asking the model to flag ambiguity (rather than guess) surfaced two real clarification points a vague prompt would have hidden.
- Specifying the output format meant the result arrived pre-structured, with no rework needed.
