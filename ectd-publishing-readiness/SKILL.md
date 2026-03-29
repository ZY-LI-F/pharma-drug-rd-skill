---
name: ectd-publishing-readiness
description: organize, regionalize, and preflight ectd submissions for fda and nmpa using official technical specifications, module 1 requirements, validation rules, sequence strategy, and transmission expectations. use when the user needs a submission assembly plan, an ectd readiness checklist, a region-specific module map, or a triage of likely validation and publishing failures.
---

# eCTD Publishing Readiness

## Overview

Use this skill when the core question is **how to assemble, validate, regionalize, and sequence an eCTD submission**. This skill assumes the scientific content already exists or is being prepared elsewhere. It focuses on publishing readiness, technical packaging, and region-specific submission behavior.

## Core principle

Always separate:
- **content adequacy** from **publishing adequacy**
- **shared CTD structure** from **regional Module 1 requirements**
- **technical validation success** from **regulatory acceptance or review success**

A technically valid eCTD can still be scientifically weak, and a strong dossier can still fail publishing requirements.

## Default workflow

1. Identify the submission region and type:
   - FDA or NMPA
   - new application, amendment, supplement, report, or lifecycle sequence
2. Determine the target standard:
   - FDA-supported eCTD version and regional M1 expectations
   - current NMPA eCTD technical specifications and implementation scope
3. Build the assembly plan:
   - module mapping
   - regional administrative documents
   - sequence strategy
   - validation and sign-off steps
4. Produce a preflight checklist focused on technical failure points.
5. End with a go or no-go publishing recommendation.

## Output contract

### 1. Submission framing
State:
- region
- application type
- lifecycle status
- target eCTD version or local specification set

### 2. Module map
| module | content owner | status | region-specific notes |
|---|---|---|---|

### 3. Publishing-risk checklist
Cover at least:
- module 1 completeness
- regional forms and administrative files
- leaf titles and placement rules
- backbone and metadata consistency
- validation readiness
- file format and document-level consistency
- sequence strategy and lifecycle operators where relevant
- transmission or portal constraints where relevant

### 4. Likely failure points
List concrete technical or organizational reasons the sequence may fail validation or intake.

### 5. Publish decision
- publish now
- publish after technical fixes
- do not publish until content and publishing gaps are separated and resolved

## Region-specific rules

### FDA
- Use only FDA-supported eCTD standards and technical conformance expectations.
- Distinguish v3.2.2 and v4.0 pathways carefully.
- Treat Module 1 as FDA-specific, even where the rest of the CTD is shared.
- Never claim that successful technical validation guarantees filing acceptance or review adequacy.

### NMPA / CDE
- Use the current CDE eCTD technical specification, validation standard, implementation guide, and published implementation scope.
- Respect the current scope of applications allowed or encouraged in eCTD format.
- Separate eCTD packaging obligations from any parallel paper or local operational requirements when applicable.
- Use current CDE module and format notices, not EMA or FDA habits, to decide local administrative structure.

## Prohibited shortcuts

Do not:
- treat FDA and NMPA module 1 as interchangeable
- assume a generic CTD folder layout is enough for a valid eCTD
- use GitHub examples as a publishing standard
- present a submission as ready if sequence planning is missing

## Good requests

- "Build an FDA eCTD readiness checklist for this IND amendment."
- "Map what changes are needed to regionalize this dossier for NMPA eCTD."
- "Why is this submission package likely to fail validation or intake?"
- "Create a preflight workflow for eCTD publishing and sign-off."

## Handoffs

- If the real issue is weak CMC content, hand off to `cmc-dossier-planner`.
- If the real issue is site and manufacturing-system readiness, hand off to `gmp-quality-readiness`.
