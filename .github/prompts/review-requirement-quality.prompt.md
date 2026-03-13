---
name: Review Requirement Quality
description: "Review FR/UC/NFR quality for completeness, consistency, testability, and traceability; report prioritized findings."
argument-hint: "Files or package scope to review"
agent: "requirements-engineer"
---
Perform a requirement quality review for the requested scope.

Review dimensions:
- Completeness (actors, triggers, flows, criteria, scope)
- Consistency (terminology, status/priority vocabulary, ID format)
- Testability (clear Given/When/Then acceptance criteria)
- Traceability (FR/UC/NFR/diagram/test links by ID)
- Method quality (single-file-first workflow, template adherence)

Output format:
1. Findings ordered by severity with file references
2. Concrete remediation for each finding
3. Open questions and assumptions
4. Optional change summary

Rules:
- Prioritize bugs/risks/regressions and missing tests first.
- Do not rewrite entire documents unless asked.
- Keep findings concise and actionable.
