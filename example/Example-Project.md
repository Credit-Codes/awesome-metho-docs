Example Project: Identity & Billing
===================================

Overview
--------
- Packages: Identity, Billing, Notifications.
- Illustrative IDs only; replace with your own.

Registry entries (sample)
-------------------------
- FR-Registry/FRs.md rows:
  - FR-ID-001 | Identity | Passwordless email sign-in | Draft
  - FR-ID-002 | Identity | Device binding enforcement | Draft
  - FR-BI-001 | Billing  | Generate monthly invoice | Draft
- UC-Registry/UCs.md rows:
  - UC-ID-Login | Identity | Magic-link login | Draft
  - UC-BI-ViewInvoice | Billing | Customer views invoice | Draft

Sample FR (Identity)
--------------------
File: Package1/FR-ID-001.md
- Description: System shall authenticate a user via passwordless email magic link valid for 10 minutes.
- Acceptance Criteria (Given/When/Then): success with valid token, reject expired token, reject reused token.
- Traceability: Related UCs: UC-ID-Login; Tests: TC-Login-001; Related FRs: FR-ID-002.

Sample UC (Identity)
--------------------
File: Package1/UC-ID-Login.md
- Actors: End User, Email Service.
- Trigger: User requests magic link.
- Main flow: request link, receive email, follow link, system verifies token, user signed in.
- Alternates: expired token, reused token.
- Impacted NFRs: NFR-2 Performance (latency), NFR-4 Security (token replay protection).
- Related FRs: FR-ID-001, FR-ID-002.

Gap analysis linkage
--------------------
- Capability: Identity & Access Mgmt; Current solution lacks device binding; To-Be includes FR-ID-002.
- Gap row cites FR-ID-002 and UC-ID-Login; remediation: add device fingerprint validation.
