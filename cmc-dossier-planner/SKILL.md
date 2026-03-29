---
name: cmc-dossier-planner
description: prepare chemistry manufacturing and controls plans, gap reviews, and module mapping for fda and nmpa drug submissions using official cmc, quality, and ctd or ectd expectations. use when the user needs a phase-appropriate cmc checklist, an ind nda bla or china registration dossier plan, a change-impact review, or a product-specific list of missing quality data.
---

# CMC Dossier Planner

## Overview

Use this skill to turn a drug-development question into a **submission-oriented CMC plan**. The goal is not to repeat generic CTD headings, but to determine what quality information is expected **now**, what can wait until a later phase, what is product-type-specific, and how the answer differs between FDA and NMPA.

This skill is especially useful for:
- pre-IND / IND quality planning
- NDA / BLA / ANDA style module planning
- NMPA clinical or marketing application CMC planning
- product lifecycle change planning
- gap assessments before dossier assembly

## Core principle

Always distinguish these four layers:

1. **Legal or regulatory baseline**
2. **Guidance recommendation**
3. **Product-type-specific expectation**
4. **Sponsor implementation choice**

Never collapse them into a single undifferentiated checklist.

## Default workflow

1. Normalize the product context:
   - small molecule, peptide, biologic, vaccine, gene therapy, cell therapy, or combination
   - drug substance and drug product status
   - phase or filing type
   - market region: FDA, NMPA, or both
2. Determine the dossier context:
   - IND / NDA / BLA / ANDA / DMF for FDA
   - clinical trial application / marketing authorization / supplement for NMPA
3. Map the request to the relevant quality framework:
   - CTD or eCTD module structure
   - phase-appropriate CMC expectations
   - lifecycle or post-change expectation when relevant
4. Produce a **gap-oriented output** rather than a topic dump.
5. Flag where modality-specific guidance is required and cannot be inferred from a generic template.

## Output contract

Always return these sections.

### 1. Regulatory framing
State:
- region and application type
- whether the answer is phase-appropriate or marketing-application-level
- whether a product-type-specific guidance is still needed

### 2. CMC workstream table
| workstream | current expectation | current evidence status | missing items | risk if omitted |
|---|---|---|---|---|
| drug substance | | | | |
| drug product | | | | |
| analytical methods | | | | |
| specifications | | | | |
| reference standards | | | | |
| container closure | | | | |
| stability | | | | |
| manufacturing process and controls | | | | |
| comparability or change control | | | | |

Adapt rows when the product requires sterility, potency, adventitious agent control, viral safety, extractables and leachables, or other specialized sections.

### 3. Module map
Provide a practical CTD or eCTD module map. For FDA and NMPA together, separate shared modules from region-specific Module 1 expectations.

### 4. Critical gaps and sequence
List the top missing quality items in the order they should be closed.

### 5. Decision note
End with a go, conditional-go, or not-ready note.

## Decision rules

- **For FDA IND**: keep the focus on sufficient CMC to assure identity, quality, purity, and strength for the current investigation; do not impose full commercial expectations too early.
- **For Phase 1 manufacturing questions**: account for FDA’s phase 1 CGMP flexibility without implying that documentation can be casual.
- **For NMPA**: respect CDE filing and format requirements, and separate CTD content expectations from eCTD packaging expectations.
- **For NMPA and FDA comparisons**: present the overlap first, then region-specific deltas.
- **For change assessments**: distinguish established knowledge, registered conditions, and changes that may trigger additional comparability or filing consequences.
- **For modality-specific products**: state clearly when a dedicated product-type guidance is needed.

## Prohibited shortcuts

Do not:
- claim that one universal CMC template fits all product types
- imply that GitHub examples are regulatory precedent
- state that FDA and NMPA always expect identical content
- treat eCTD publishing as a substitute for CMC adequacy

## Good requests

- "Build a phase-appropriate CMC gap assessment for a small-molecule IND package for FDA."
- "Map the CMC dossier work needed before a China marketing application for this biologic."
- "Compare FDA and NMPA CMC expectations for a post-change analytical package."
- "What quality sections are still too weak for filing readiness?"

## Handoffs

- If the question is mainly about submission packaging, sequence handling, validation, or module 1 assembly, hand off to `ectd-publishing-readiness`.
- If the question is mainly about site systems, batch release governance, deviations, CAPA, data integrity, or inspection readiness, hand off to `gmp-quality-readiness`.
