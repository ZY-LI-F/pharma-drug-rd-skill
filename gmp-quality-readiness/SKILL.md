---
name: gmp-quality-readiness
description: assess gmp or cgmp readiness, build quality-system checklists, and summarize inspection or filing risks for fda and nmpa regulated drug manufacturing using official quality-system, cgmp, and gmp requirements. use when the user needs a site readiness review, a deviation capa and release-governance checklist, a phase-appropriate manufacturing control plan, or a region-specific quality gap summary.
---

# GMP Quality Readiness

## Overview

Use this skill to evaluate whether a manufacturing site, quality system, or batch-control process is ready for the requested development or commercial stage. This skill is not a substitute for a formal audit, but it is designed to produce a **regulator-facing readiness view** that aligns with official FDA and NMPA requirements.

## Core principle

Always separate:
- **baseline GMP or cGMP obligations**
- **phase-specific flexibility**
- **site practice that is acceptable but not ideal**
- **inspection-risk issues that can block use or release**

## Default workflow

1. Identify the operating context:
   - development stage: phase 1, later clinical, commercial, tech transfer, post-approval
   - product type: sterile, non-sterile, biologic, small molecule, high-potency, etc.
   - region: FDA, NMPA, or both
2. Determine the quality-system scope:
   - organization and independence of quality
   - document control
   - change control
   - deviation and investigation
   - CAPA
   - validation and qualification
   - data integrity and record control
   - laboratory control
   - batch disposition and release
   - supplier and material controls
3. Assess each area as:
   - acceptable
   - acceptable with remediation
   - significant risk
   - unacceptable for current stage
4. End with a remediation sequence tied to inspection or filing risk.

## Output contract

### 1. Readiness summary
One short paragraph with a status:
- ready
- conditionally ready
- not inspection-ready
- not filing-supportive

### 2. System assessment table
| quality area | status | main issue | consequence | recommended action |
|---|---|---|---|---|

### 3. High-risk observations
List issues likely to create major regulatory concern, such as:
- missing independence of quality oversight
- batch release without adequate review
- uncontrolled deviations or CAPA backlog
- incomplete validation or qualification rationale
- poor raw-data control or audit-trail governance
- unclear link between registered process and executed process

### 4. Remediation sequence
Give the practical order of correction, not just the topic list.

## Decision rules

- **FDA**: anchor site expectations in current good manufacturing practice, quality system thinking, and phase-specific flexibility when justified.
- **FDA phase 1**: acknowledge that full 21 CFR part 211 compliance is not universally imposed in the same way for phase 1 investigational drugs, but quality control principles and subject protection still matter.
- **NMPA**: anchor the analysis in the drug GMP framework and registration-linked quality obligations.
- **For both regions**: treat data integrity, document control, and batch traceability as cross-cutting system controls.
- **For sterile or biologic products**: explicitly note that generic GMP summaries are insufficient without product-type-specific controls.

## What to avoid

Do not:
- reduce GMP to a document checklist only
- describe CAPA as optional or cosmetic
- imply that a site can compensate for weak systems with a strong dossier alone
- merge phase-appropriate flexibility into a claim that controls can be informal

## Good requests

- "Assess whether this pilot site is GMP-ready enough to support phase 1 clinical supply."
- "Give me a gap summary for FDA and NMPA inspection-sensitive quality systems."
- "What are the highest-risk GMP weaknesses in this deviation and release workflow?"
- "Build a remediation sequence for a site before filing-support activities begin."

## Handoffs

- If the issue is mainly about submission modules or dossier assembly, hand off to `cmc-dossier-planner`.
- If the issue is mainly about eCTD structure, module 1 regionalization, validation, or sequence planning, hand off to `ectd-publishing-readiness`.
