# Personal AI Integration Plan

The following plan describes realistic ways I can use generative AI as a Business Analyst on GovConnect-type work, while keeping accuracy, confidentiality, and final decisions under human control.

| Recurring Task | Expected Benefit | Preferred Prompt or Workflow | Main Risk / Verification Requirement | Frequency | What Success Looks Like |
|---|---|---|---|---|---|
| Turn UAT/status meeting notes into a decision-ready brief | Expected to save time and reduce the chance of missed action items or decisions | Use the Meeting Notes → Decision-Ready Brief prompt, then follow Raw Input → Prompt → AI Output → Human Review → Final Output | AI may invent owners, deadlines, or turn open questions into decisions. Compare every name, date, and decision against the raw notes | After each status/UAT meeting | A brief is ready within 20 minutes, every fact matches the source, and no owner/deadline is invented |
| Draft stakeholder communications (schedule changes, updates) | Expected to produce a usable first draft faster and keep tone consistent across audiences | Use a C.A.R.E.-structured prompt like the Stakeholder Delay Update Email, then Draft → Verify → Refine → Human Sign-off | Unconfirmed claims (e.g., stating impact that wasn't verified) or an inappropriate tone. Check every fact before sending; never mark as approved without review | One to three times per week, as needed | The final email is accurate, concise, and explicitly approved before it goes to stakeholders |
| Draft user stories and UAT test cases from feature requests | Expected to speed up turning a stakeholder request into testable criteria and surface ambiguity earlier | Use the User Story & Acceptance Criteria Drafter, then the UAT Test Case Builder prompt | AI may assume undescribed functionality or UI behavior. Flag every assumption as an open question for stakeholder confirmation rather than guessing | During each new feature/requirements cycle | Stories are testable, acceptance criteria are specific, and open questions are confirmed with stakeholders before UAT begins |

## Habits I Will Build
1. Start every AI task with a C.A.R.E. or R.C.T.O.-structured prompt instead of a vague request.
2. Use only fictional or properly anonymized details, consistent with the Green/Amber/Red classification in the Responsible AI section.
3. Keep the raw source next to the AI output during verification, as practiced in the Information Workflow and Verification sections.
4. Mark missing information as `[Not Specified]` rather than letting AI guess.
5. Never mark a stakeholder-facing output as human-approved without an actual review.
6. Revisit and improve saved prompts based on how well they perform in real use.
