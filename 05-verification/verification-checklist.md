# Verification Checklist

## My Personal Checklist
Before using or sharing AI-generated workplace content, I will:
1. Identify the content type, intended audience, and risk level.
2. Cross-check every name, date, and number against the raw source.
3. Confirm every listed decision is an actual decision — not a suggestion or open question mistaken for one.
4. Confirm every owner and deadline is either sourced or explicitly marked `[Not Specified]`.
5. Check that priority/urgency ratings are still accurate, including against anything decided in other parts of the portfolio.
6. Confirm no confidential, private, or sensitive information is included.
7. Record findings and corrections, and get human approval before final use.

## Worked Example

**Output selected:** the Final Structured Output from [Information Workflow](../03-information-workflow/information-processing-example.md).

| Check | What I Tested | Finding | Action Taken |
|---|---|---|---|
| Content and audience | A UAT status brief for the project sponsor | Correct format and audience level for a sponsor-facing brief | Kept unchanged |
| Names, dates, numbers | "Wednesday," "Finance," "two critical bugs," "end of week" | All match the raw input exactly | Kept unchanged |
| Decisions vs. open questions | License-renewal scope; go/no-go decision | Both correctly kept as open/pending, not stated as decided | Kept unchanged |
| Owners and deadlines | Accessibility review owner; bug-fix deadline | Correctly marked `[Not Specified]` where the source gave no owner/date | Kept unchanged |
| Priority accuracy | "Complete accessibility review" — rated Medium originally | The Planning Workflow now treats this as a blocker for the pilot phase — Medium no longer reflects its actual urgency | Corrected to High in the Information Workflow, to stay consistent with the Planning Workflow |
| Sensitive information | Department names, generic role names, no citizen data | No real confidential or personal data present | Confirmed safe |
| Human approval | Full brief, after the above checks | Corrections applied and consistent across sections | Reviewed and approved |

## Verification Result
The brief was largely accurate and well-sourced, but one item — the accessibility-review priority — was inconsistent with a dependency established later, in the Planning Workflow. This is exactly the kind of cross-section inconsistency a verification pass is meant to catch, not just factual errors within a single document. I corrected the Information Workflow's priority rating from Medium to High as a result.

**Final decision:** Approved. The corrected brief (with the accessibility-review priority updated to High) is confirmed accurate and ready for inclusion in the portfolio.
