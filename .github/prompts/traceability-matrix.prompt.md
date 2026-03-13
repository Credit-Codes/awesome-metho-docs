---
name: Traceability Matrix
description: "Build or update a traceability matrix across FR, UC, NFR, tests, and diagrams using IDs."
argument-hint: "Scope (package or repo), source files, and target artifact to update"
agent: "requirements-engineer"
---
Build or update a requirements traceability matrix for the specified scope.

Instructions:
- Use IDs as primary keys (FR-*, UC-*, NFR-*).
- Capture both coverage and missing links.
- Do not invent IDs; flag missing artifacts as gaps.

Required matrix columns:
1. FR ID
2. Linked UC IDs
3. Linked NFR IDs
4. Linked diagrams
5. Linked tests
6. Coverage status (Covered/Partial/Missing)
7. Notes and gaps

Quality checks before finalizing:
- No title-only references in place of IDs.
- Missing links are explicitly marked, not silently omitted.
- Matrix entries are deduplicated and consistent.
