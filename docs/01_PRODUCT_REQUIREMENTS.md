# Skyra Document Generation Service — Product Requirements

## Maintained specification — current status

Updated 2026-10-14. This is one of the nine initial project documents and must be retained and updated in place. Remove only redundant per-work reports; do not replace or delete the initial specification set.

Specification only; no generation/validation service implemented.

The following references hold the detailed current implementation; requirements and proposed designs below must not be read as already built:

- [Current architecture and database design](ARCHITECTURE.md)
- [Current functionality and implementation boundaries](FUNCTIONALITY.md)
- [Current milestone and verification summary](DEVELOPMENT.md)

Prepared: 2026-10-14. Requirement/design baseline. Use the maintained current-status section above to distinguish implemented work from planned work.

## Product overview

Creates editable project and business documents from structured briefs and templates, with rendering, validation and traceable deliverables.

## Problem and current baseline

Initial baseline: documentation-only project at the time of specification; current implementation status is stated above. Jarvis currently has basic Office edits, not a complete document-generation and verification service.

Existing prototypes do not establish production readiness. The objective is a reusable, testable boundary with explicit ownership and verifiable outcomes.

## Target users and goals

Primary users: Skyra owner and authorized employees; consuming applications and delegated agents act under those users' scoped identities. Commercial customers use separately branded products rather than inheriting internal Jarvis privileges.

Success means the capabilities below pass recorded acceptance checks, survive expected failures and expose enough evidence for a human to review the result.

## Core requirements / MVP

- **FR-01:** Markdown, DOCX, PDF, XLSX and PPTX job profiles introduced incrementally
- **FR-02:** Versioned templates, brand profiles and source references
- **FR-03:** Project document sets generated from one consistent requirements model
- **FR-04:** Formula and document-structure validation plus visual render checks
- **FR-05:** Local file delivery and explicit Google export/save operations
- **FR-06:** Artifact versioning, content hashes and reproducible generation manifests

## Boundaries

This project delivers its declared capabilities only. No automatic production release, account creation, purchase or broader permission is implied by an AI plan. Article-dashboard implementation, ERP, Skyra Platform and QR changes are outside this documentation initiative. Future local models and hosted Jarvis must preserve the same authorization contracts.

## User journey

An authorized caller selects a capability and resource scope, submits validated input, receives either a result or a durable job reference, follows progress and retrieves evidence. Policy may require an exact-action approval before execution. Failures present recovery guidance without claiming success.

## Acceptance and unresolved decisions

See [testing](08_TESTING_AND_ACCEPTANCE.md) for release evidence and [tasks](05_PROJECT_TASKS.md) for implementation sequence.

- openpyxl-style libraries do not calculate formulas by themselves
- Renderer/font availability affects output and must be pinned
- Financial values are supplied by ERP business rules, not invented by a generation agent
