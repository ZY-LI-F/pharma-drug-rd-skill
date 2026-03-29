---
name: target-evidence-triage
description: synthesize target discovery and target validation evidence for a disease, pathway, gene, biomarker, or drug hypothesis. use when the user needs a ranked target shortlist, a mechanism summary, or an evidence-backed go no-go view built from drugclaw style drug-target, mechanism, disease-gene, pharmacogenomics, and clinical signals.
---

# Target Evidence Triage

## Overview

Turn a target idea into an evidence-backed prioritization brief. This skill is optimized for computational target discovery and validation, especially when the user starts with a disease, pathway, gene family, biomarker, or an already-known drug and needs to decide which targets deserve follow-up.

## Default workflow

1. Normalize the request into disease, indication, target candidates, drugs, biomarkers, and decision question.
2. Build an evidence matrix with these columns: target, disease rationale, druggability evidence, mechanism evidence, pharmacogenomics flags, clinical evidence, contradictions, and confidence.
3. Separate evidence into direct, indirect, and weak-support buckets.
4. Rank candidates with an explicit rationale, not only a score.
5. End with the next experiments or analyses needed to de-risk the top 1 to 3 targets.

## Inputs to request or infer

- disease or phenotype
- candidate targets or target family, if any
- known drugs, tool compounds, biomarkers, or pathways
- decision type: shortlist, compare, rebuttal, or due diligence
- desired output depth: one-page brief or full evidence table

## Output contract

Always return:

### 1. Decision summary
- one paragraph
- 1 to 3 recommended targets or a no-go statement

### 2. Evidence table
| target | why it matters | direct evidence | indirect evidence | liabilities | confidence |

### 3. Contradictions and missing evidence
List conflicts across sources, data sparsity, and assumptions.

### 4. Next-step plan
Use action verbs such as validate, benchmark, dock, assay, stratify, or deprioritize.

## Heuristics

- Prefer direct target-disease or target-drug evidence over broad pathway mentions.
- Treat disease-gene association alone as insufficient for target nomination.
- Promote targets with convergent support from mechanism, pharmacogenomics, and clinical evidence.
- Downgrade targets with strong toxicity, DDI, or label-based liabilities unless the user explicitly wants risky moonshots.
- If evidence is mostly literature- or ontology-level, say so plainly.

## Good requests

- "Prioritize kinase targets for EGFR-TKI resistant NSCLC and explain why the top 3 beat the rest."
- "Compare JAK1, TYK2, and BTK for autoimmune repurposing potential."
- "Given this biomarker panel, which druggable targets deserve validation next?"

## Escalation rules

- If the user needs structure prediction or docking, hand off to `structure-folding-planner` or `virtual-screening-orchestrator`.
- If the user needs indication expansion, hand off to `repurposing-hypothesis-screen`.
- If the user needs safety translation, hand off to `safety-pgx-brief`.
