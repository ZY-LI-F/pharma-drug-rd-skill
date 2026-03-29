---
name: clinical-study-ops
description: prepare clinical data capture and trial operations plans using openclinica style workflows. use when the user needs a study setup checklist, ecrf and visit design plan, data management handoff, or a pragmatic open-source edc workflow for translational and clinical studies.
---

# Clinical Study Ops

## Overview

Use this skill when a discovery or translational program is moving into structured clinical data capture. It is optimized for trial operations planning, not biostatistics or submission writing.

## Workflow

1. Identify study type, population, intervention, endpoints, and operational constraints.
2. Convert the protocol summary into operational objects: sites, visits, eCRFs, edit checks, roles, and data exports.
3. Build a minimum viable EDC plan.
4. Flag operational risks such as ambiguous endpoints, missing edit checks, or weak auditability.
5. Output a study-ops checklist and build order.

## Output structure

### Study setup table
| object | decision |
| study | |
| visits | |
| ecrfs | |
| edit checks | |
| user roles | |
| exports | |

### Operational risks
List anything likely to cause rework later.

### Build order
Give the sequence for standing up the study in an EDC/CDM system.

## Rules

- Keep the output operational and auditable.
- If the user asks for protocol design, distinguish protocol content from EDC implementation.
- If the user asks for trial evidence synthesis rather than operations, use a DrugClaw-style evidence skill instead.

## Good requests

- "Turn this phase II study concept into an OpenClinica-style build checklist."
- "What eCRFs and edit checks are required for this biomarker-enriched trial?"
- "Create a minimum viable clinical data management plan for this translational study."
