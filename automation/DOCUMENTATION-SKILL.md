Documentation Skill
===================

Purpose
-------
Use this skill when documenting requirements in this repository. It provides a map of where each artifact lives and exact instructions for what to update.

Audience
--------
- SWEs and analysts writing requirements.
- AI agents generating or updating artifacts.
- Reviewers validating traceability and quality.

When to use this skill
----------------------
Use this skill for any task that creates or updates:
- FRs
- UCs
- NFR references
- Analysis entries
- Entity documentation (DDT + PlantUML)
- Gap analysis rows

Repo map and what each area does
--------------------------------

Top-level governance
- `AGENTS.md`: guardrails, canonical status/priority vocabulary, and behavior constraints for agents.
- `SCHEMA.md`: ID formats, naming, registry rules, and traceability conventions.
- `QUALITY-GUIDE.md`: quality checklist for readiness.
- `ANALYSIS-STANDARD.md`: mandatory analysis workflow and handoff sections.
- `WORKFLOWS.md`: operational procedures for FR/UC/entity/gap updates.
- `PROMPTS.md`: reusable prompt patterns for analysis and drafting.

Core working files
- `Analysis/Analysis.md`: analysis registry and template; first stop for incoming requirements.
- `NFRs.md`: project-level NFR definitions referenced by UCs.
- `FR-Registry/FRs.md`: FR registry and FR template section.
- `UC-Registry/UCs.md`: UC registry and UC template section.
- `Data/Entities.md`: cross-package entity registry and aggregate DDT template.
- `ENTITY-GUIDE.md`: entity rules for DDT and PlantUML synchronization.

Package-level implementation
- `Package1/`, `Package2/`, `Package3/` (or renamed package folders):
  - `Entities.md`: package entity classification + attribute-level DDT + PlantUML.
  - `FR-*.md`: one FR artifact per file.
  - `UC-*.md`: one UC artifact per file.

Supporting areas
- `Diagrams/`: behavioral/structural diagram storage.
- `PM/README.md`: project charter and management framing.
- `example/`: sample project outputs and structure references.
- `automation/`: automation aids and workflow support docs.

Task-to-file instruction map
----------------------------

If task is: Analyze new requirement input
1) Update `Analysis/Analysis.md`:
   - Fill Analysis Identification.
   - Add Source Summary.
   - Add Candidate Requirement rows.
   - Add Ambiguity/Questions.
   - Add Traceability Preview.
   - Add Recommended File Updates.
2) Keep status as Draft if open questions remain.

If task is: Create or update an FR
1) Update `FR-Registry/FRs.md` with FR row (ID, package/module, title, status).
2) Create/update package FR file with matching filename and ID.
3) Fill FR sections:
   - Identification
   - Description ("system shall")
   - Acceptance Criteria (Given/When/Then rows)
   - Constraints
   - Traceability (related UCs/tests/design)
4) Ensure related entities are covered in package and global entity registries.

If task is: Create or update a UC
1) Update `UC-Registry/UCs.md` with UC row.
2) Create/update package UC file with matching filename and ID.
3) Fill UC sections:
   - Identification
   - Preconditions
   - Trigger
   - Main flow (3-7 steps)
   - Alternate/Error flows
   - Postconditions
   - Business rules
   - NFR impact section
4) Include related FR IDs and ensure reciprocal FR traceability is updated.

If task is: Document entities
1) Update package `Entities.md`:
   - Entity classification rows with role (Core/Column/Complementary).
   - Attribute-level DDT rows with full standard columns.
   - PlantUML aligned with DDT entity set.
2) Update `Data/Entities.md` for package mapping and source FR/UC references.

If task is: Capture NFR impacts
1) Reference NFR IDs in UC section 9.
2) If new NFRs are needed, update `NFRs.md` first, then reference IDs from UCs.

If task is: Record a gap
1) Add gap row in the agreed gap matrix/document for the project.
2) Include As-Is, To-Be, gap type, business impact, remediation.
3) Cite FR/UC IDs to keep traceability explicit.

Do/Do-not rules
---------------
Do:
- Keep IDs stable and filename-matched.
- Keep templates intact; fill fields and append rows.
- Use canonical vocabulary: Status (Draft | In Review | Approved | Deprecated), Priority (Must | Should | Could).
- Ask for clarification when actor/trigger/acceptance criteria/priority/release is missing.

Do not:
- Delete IDs or rename published artifacts.
- Perform bulk template rewrites.
- Replace ID references with title-only references.
- Invent missing facts; keep unresolved items explicit.

Completion checklist
--------------------
Before handoff, confirm:
- Analysis entry exists for new input.
- Registry rows and artifact files are in sync.
- FR <-> UC links are reciprocal.
- UC NFR references are present where applicable.
- Entities are reflected in both package and global registries.
- DDT rows and PlantUML describe the same entity set.
- Status and priority values use canonical enums.
