Automation Aids
===============

Documentation skill
-------------------
- See `DOCUMENTATION-SKILL.md` for the repository map and task-to-file instructions for SWEs and agents.
- Use it as the default playbook when creating/updating Analysis, FR, UC, NFR references, entity docs, and gap rows.

ID regex (suggested)
--------------------
- FR IDs: `FR-[A-Z]{2,}-\d{3}`
- UC IDs: `UC-[A-Z]{2,}[A-Za-z0-9-]*`
- Test IDs: `TC-[A-Z]{2,}-\d{3}`

Status/priority constants
-------------------------
- Status: Draft | In Review | Approved | Deprecated.
- Priority: Must | Should | Could.

Pre-commit ideas (manual or hook)
---------------------------------
- Block commits if FR/UC filenames do not match their ID patterns.
- Warn if registries lack rows for new FR/UC files.
- Warn if traceability tables miss reciprocal links (FR lacks UC that cites it).

Future automation hooks
-----------------------
- Script to add registry rows from new files.
- Lint to ensure Given/When/Then rows exist in FR acceptance criteria.
- Lint to ensure UC main flow has at least 3 steps.
