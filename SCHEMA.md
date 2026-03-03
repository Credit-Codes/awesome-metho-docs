Schema and Conventions
======================

IDs
---
- Analysis IDs: AN-<DomainCode>-<NNN> (e.g., AN-ID-001).
- Entity IDs: ENT-<DomainCode>-<NNN> (e.g., ENT-ID-001).
- FR IDs: FR-<DomainCode>-<NNN> (e.g., FR-ID-001). Stable once published.
- UC IDs: UC-<DomainCode>-<NNN> (e.g., UC-ID-Login).
- Test IDs: TC-<Area>-<NNN> (when referenced).
- Requirement Code (inside FR): [FR-…-NNN] Short Name, mirrors the file ID.

Status enums
------------
- Draft | In Review | Approved | Implemented | Deprecated.

Priority enums
--------------
- Must | Should | Could.

File naming
-----------
- One major artifact per file; filename matches the ID (e.g., FR-ID-001.md).
- Keep templates; duplicate them when adding new artifacts.

Registry rules
--------------
- Analysis/Analysis.md: one row per analysis effort with source, scope, owner, and status.
- Data/Entities.md: one row per entity with package mapping and diagram reference.
- FR-Registry/FRs.md: one row per FR with package/module, title, status.
- UC-Registry/UCs.md: one row per UC with domain, actor, status.
- Registries must reflect any new or changed artifact immediately.

Entity documentation rules
--------------------------
- Every package maintains PackageX/Entities.md.
- Entities use DDT (Data Dictionary Table) columns as defined in ENTITY-GUIDE.md.
- Each package classifies entities as Core, Column, or Complementary.
- Each package entity file includes a PlantUML diagram reflecting documented entities.
- DDT rows are attribute/column-level and include: Key (PK/FK/-), Data Type, Not Null (Y/N), Length, FK Table, Description.

Traceability rules
------------------
- UC files list Related FRs (IDs) and impacted NFRs.
- FR files list Related UCs, related FRs, design components, and test cases.
- Gap matrix rows cite FR/UC IDs to show coverage or gaps.

Acceptance criteria
-------------------
- Use Given/When/Then tables.
- Cover success, boundary, and failure where applicable.

NFR references
--------------
- Reference NFR IDs in UC section 9 when the flow depends on them.

Link hygiene
------------
- Use relative links within markdown when adding explicit links; keep IDs consistent with filenames.
