---
name: Gap Analysis
description: "Produce a methodical As-Is vs To-Be gap analysis tied to FR/UC IDs with impact and remediation."
argument-hint: "Business process scope, current state, target state, and related FR/UC IDs"
agent: "business-analyst"
---
Create a gap analysis for the requested scope.

Instructions:
- Compare current process (As-Is) and desired process (To-Be) step by step.
- Identify coverage gaps against existing FR/UC artifacts.
- Use explicit business impact and clear remediation recommendations.
- Ask clarifying questions when scope boundaries are unclear.

Output table columns:
1. Gap ID
2. Related IDs (FR/UC/NFR)
3. As-Is
4. To-Be
5. Gap type
6. Business impact
7. Recommended remediation
8. Priority
9. Owner suggestion

Quality checks before finalizing:
- Every gap row cites at least one FR or UC ID when applicable.
- Impact and remediation are concrete and testable.
- Ambiguities are listed separately as open questions.
