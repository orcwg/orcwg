# Document Metadata

This document defines the frontmatter schemas used across this repository for meeting minutes and deliverables.

## Conventions

- Frontmatter is YAML enclosed in `---` fences at the very top of the file.
- All dates use ISO 8601 format: `YYYY-MM-DD`.
- Field names are **case-sensitive** and use the exact capitalization shown
  (e.g. `Document type`, not `Document Type`).
- A `*` after a field name marks it as required. All other fields are optional or conditional (see the field's description).
- Optional fields may be omitted or left empty when they don't apply.
- Status values include their leading emoji as shown.

## Document types

Every content document declares a `Document type`. The valid values are:

| Document type        | Schema                                                           |
| ---------------------- | ---------------------------------------------------------------- |
| `Minutes`              | [Minutes](#minutes)                                              |
| `Liaison meeting notes`| [Liaison meeting notes](#liaison-meeting-notes)                  |
| `Submission`           | [Submission](#submission)                                        |
| `White paper`          | [White paper](#white-paper)                                      |
| `Specification`        | [Specification](#specification)                                  |

---

## Minutes

For meetings of the SIG, a task force, or a governance committee. Notes from meetings with external bodies use a different schema (see [Liaison meeting notes](#liaison-meeting-notes)).

| Field          | Value                                                | Notes                                                          |
| -------------- | ---------------------------------------------------- | -------------------------------------------------------------- |
| Document type* | `Minutes`                                            |                                                                |
| SIG            | `Cyber Resilience SIG` \| `AI Policy and Compliance SIG` | Required for SIG meetings or for meetings of their task forces |
| Task force     | Name of the task force                               |                                                                |
| Committee      | `Steering Committee` \| `Specification Committee`    | Required for governance meetings                               |
| Status*        | See [Meeting notes lifecycle](working-mode.md#meeting-notes-lifecycle) |                                                                |
| Date*          | `YYYY-MM-DD`                                         | Date of the meeting                                            |
| Approved       | `YYYY-MM-DD`                                         | Date the minutes were approved. Set when `Status` becomes `✅ Approved` |

Exactly one of `SIG` or `Committee` must be set.

SIG plenary meeting:

```yaml
---
SIG: Cyber Resilience SIG
Document type: Minutes
Status: ✅ Approved
Date: 2026-02-02
Approved: 2026-02-16
---
```

Task force meeting:

```yaml
---
SIG: Cyber Resilience SIG
Task force: FAQ TF
Document type: Minutes
Status: 🗓️ Proposed agenda
Date: 2026-10-31
---
```

Governance committee meeting:

```yaml
---
Committee: Steering Committee
Document type: Minutes
Status: ✅ Approved
Date: 2026-02-12
Approved: 2026-03-12
---
```

File naming: `YYYY-MM-DD-mom-[group-name].md`. Located in:

- `[sig]/minutes/` for SIG plenary
- `[sig]/task-forces/[task-force]/minutes/` for task forces
- `governance/[committee]/minutes/[year]/` for governance committees

---

## Liaison meeting notes

For notes from meetings held with external liaison groups (e.g. CEN/CENELEC PT 3 sessions). These are **not** SIG/task force meetings and have a distinct `Document type`.

| Field          | Value                                                | Notes                          |
| -------------- | ---------------------------------------------------- | ------------------------------ |
| Document type* | `Liaison meeting notes`                              |                                |
| SIG*           | `Cyber Resilience SIG` \| `AI Policy and Compliance SIG` |                            |
| Group*         | One of the SIG's [current liaisons](cyber-resilience-sig/README.md#current-liaisons)  |                                |
| Subgroup       | E.g. `PT 3`                                          |                                |
| Date*          | `YYYY-MM-DD`                                         | Date of the meeting            |

```yaml
---
SIG: Cyber Resilience SIG
Document type: Liaison meeting notes
Group: CEN/CENELEC WG 9
Subgroup: PT 3
Date: 2025-05-21
---
```

File naming: `YYYY-MM-DD-[descriptor]-meeting-notes.md` in `[sig]/coordination/[group]/`.

---

## Deliverables

Documents the working group produces as output: submissions to external stakeholders ([Submission](#submission)), analytical white papers
([White paper](#white-paper)), and normative technical specifications ([Specification](#specification)). All three share a common set of fields
and are tracked in `[sig]/deliverables.md`.

### Common fields

Every deliverable carries these fields:

| Field          | Value                                                | Notes                                              |
| -------------- | ---------------------------------------------------- | -------------------------------------------------- |
| Document type* | `Submission` \| `White paper` \| `Specification`     |                                                    |
| SIG*           | `Cyber Resilience SIG` \| `AI Policy and Compliance SIG` |                                                    |
| Task force     | Name of the task force                               | If produced by a TF                                |
| Number*        | E.g. `2.5`                                           | Matches the deliverables plan                      |
| Status*        | See [Deliverables lifecycle](working-mode.md#deliverables-lifecycle) |                                                    |
| Date           | `YYYY-MM-DD`                                         | Date work on the document started                  |
| Deadline       | `YYYY-MM-DD`                                         | Deadline by which the document must be completed (e.g. consultation closing date) |
| Shipped        | `YYYY-MM-DD`                                         | Date the document was shipped. Set when `Status` becomes `🚀 Shipped` |
| Cancelled      | `YYYY-MM-DD`                                         | Date the document was cancelled. Set when `Status` becomes `❌ Cancelled` |

Each `Document type` adds its own fields below.

### Submission

A unit of output submitted to an external stakeholder (e.g. comments, contributions, feedback, responses).

Adds these fields to the [common set](#common-fields):

| Field    | Value                                                | Notes              |
| -------- | ---------------------------------------------------- | ------------------ |
| Editors  | Comma-separated list of names                        | Required once `Status` is `✍️ Work in Progress` or beyond. See [Editors](working-mode.md#editors). |
| Group*   | One of the SIG's or WG's current liaisons.           | Target stakeholder |
| Subgroup | E.g. `PT 3`, `Open Source Workstrand`                |                    |

```yaml
---
SIG: Cyber Resilience SIG
Document type: Submission
Number: 2.5
Status: 🚀 Shipped
Editors: Juan Rico, Tobie Langel
Group: CEN/CENELEC WG 9
Subgroup: PT 3
Date: 2025-06-11
Shipped: 2025-06-12
---
```

File naming: `deliverable-X-Y.md`, in `[sig]/coordination/[stakeholder]/`, or inside a dated subfolder (`YYYY-MM-[descriptor]/`) when the deliverable bundles supporting artifacts such as a PDF.

### White paper

A standalone analytical document intended as input to external bodies.

Adds these fields to the [common set](#common-fields):

| Field              | Value                          | Notes                |
| ------------------ | ------------------------------ | -------------------- |
| Editors            | Comma-separated list of names  | Required once `Status` is `✍️ Work in Progress` or beyond. See [Editors](working-mode.md#editors). |
| Input to*          | Free-text list                 | Intended consumers   |
| Relevant liaisons* | Free-text list                 | Liaison groups       |
| License*           | [SPDX identifier](https://spdx.org/licenses/), e.g. `CC-BY-4.0` |                      |

```yaml
---
SIG: Cyber Resilience SIG
Document type: White paper
Number: 3.5
Status: 🚀 Shipped
Editors: Mikaël Barbero
Input to: EU Guidance, Implementing Act, Harmonised standards
Relevant liaisons: EU Commission, CRA Expert Group, CEN/CENELEC, Market Surveillance
License: CC-BY-4.0
---
```

Located in `[sig]/whitepapers/`.

### Specification

A normative technical specification.

Adds these fields to the [common set](#common-fields):

| Field              | Value                          | Notes                |
| ------------------ | ------------------------------ | -------------------- |
| Maintainers        | Comma-separated list of names  | Project maintainers responsible for the spec. Specifications use `Maintainers` rather than `Editors` since they are developed by an [Eclipse open source project](working-mode.md#deliverables). |
| Input to*          | Free-text list                 | Intended consumers   |
| Relevant liaisons* | Free-text list                 | Liaison groups       |
| License*           | [SPDX identifier](https://spdx.org/licenses/), e.g. `CC-BY-4.0` | License of the working draft |
| Final license*     | [SPDX identifier](https://spdx.org/licenses/), e.g. `EFSL` | License the spec will carry once finalized |

```yaml
---
SIG: Cyber Resilience SIG
Document type: Specification
Number: 4.2
Status: 🗺️ Planned
Maintainers: Mikaël Barbero
Input to: ISO
Relevant liaisons: EU Commission, CRA Expert Group, CEN/CENELEC, Market Surveillance
License: CC-BY-4.0 OR Apache-2.0
Final license: EFSL
---
```

Located in `[sig]/proposed-specs/`.

---

\* Field names with a trailing asterisk are required. All other fields are optional or conditional (see the field's description).
