# Skyra Document Generation Service — Functionality

Last maintained: 2026-10-14. This is the canonical project requirement/capability reference. Current implementation and planned work are explicitly distinguished.

## Product and users

Creates editable project and business documents from structured briefs and templates, with rendering, validation and traceable deliverables.

Users: Skyra owner and authorized employees; service consumers act under scoped user/project/account identity. Commercial products stay independent of internal Jarvis privileges.

## Current implementation

Specification only; no generation/validation service implemented.

## Required capabilities

- Markdown, DOCX, PDF, XLSX and PPTX job profiles introduced incrementally
- Versioned templates, brand profiles and source references
- Project document sets generated from one consistent requirements model
- Formula and document-structure validation plus visual render checks
- Local file delivery and explicit Google export/save operations
- Artifact versioning, content hashes and reproducible generation manifests

## Interface direction

The following interfaces are design proposals from the project baseline, not a guarantee of working endpoints. Existing prototype routes must be checked against their source before consumer integration.

| Proposed operation | Purpose |
|---|---|
| `POST /v1/document-jobs` | Submit brief/template/output profiles; return 202 |
| `GET /v1/document-jobs/{id}` | Return generation and verification status |
| `GET /v1/templates` | List compatible template versions |
| `POST /v1/document-jobs/{id}/exports` | Export validated artifact to an authorized target |

## Acceptance requirements

- Generated files open in their supported target applications
- PDF/doc render checks find overflow, missing assets and clipped text
- Spreadsheet formulas and recalculated values are validated by a declared calculation engine
- Document set references agree on scope, architecture and milestones
- An unverified artifact is labelled draft rather than final

## Explicit boundaries and open decisions

- openpyxl-style libraries do not calculate formulas by themselves
- Renderer/font availability affects output and must be pinned
- Financial values are supplied by ERP business rules, not invented by a generation agent

A proposal, simulation or passing build does not authorize production release. Account connection, publication, money movement and employee/payroll actions obey their configured permission policies.

## Initial specification set

Retain and update the original nine documents. They describe product requirements, system architecture, development rules, design, tasks, memory, API/events, testing/acceptance and security/operations. These current overview files supplement them; they do not replace them.

- [Product requirements](01_PRODUCT_REQUIREMENTS.md)
- [System architecture](02_SYSTEM_ARCHITECTURE.md)
- [Development rules](03_DEVELOPMENT_RULES.md)
- [Design system](04_DESIGN_SYSTEM.md)
- [Project tasks](05_PROJECT_TASKS.md)
- [Project memory](06_PROJECT_MEMORY.md)
- [API and event contracts](07_API_AND_EVENTS.md)
- [Testing and acceptance](08_TESTING_AND_ACCEPTANCE.md)
- [Security and operations](09_SECURITY_AND_OPERATIONS.md)
