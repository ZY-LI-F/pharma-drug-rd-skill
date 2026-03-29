---
name: repurposing-hypothesis-screen
description: screen drug repurposing hypotheses and indication expansion ideas with evidence tables, mechanistic plausibility checks, and termination risk notes. use when the user asks whether an existing drug could treat a disease, which approved assets are most plausible for a new indication, or how to rank repurposing candidates before deeper validation.
---

# Repurposing Hypothesis Screen

## Overview

Use this skill to evaluate whether an existing drug or asset class is plausible for a new disease indication. The goal is not only to find positive signals, but also to surface why a repurposing idea may fail.

## Workflow

1. Normalize disease, phenotype, and candidate drugs.
2. Build a candidate panel from approved drugs, shelved assets, known mechanisms, and pathway neighbors.
3. For each candidate, summarize mechanism fit, disease biology fit, known target overlap, prior clinical evidence, and safety translation risk.
4. Mark each candidate as advance, watchlist, or reject.
5. Recommend the cheapest next validation step.

## Required output

### Repurposing scoreboard
| candidate | mechanism fit | evidence type | clinical maturity | safety friction | verdict |

### Failure modes
Explicitly list likely reasons for false positives such as tissue mismatch, exposure mismatch, class toxicity, or weak causal disease biology.

### Fast-follow actions
Give 3 to 5 next actions, for example:
- re-check target expression in disease tissue
- compare exposure against known efficacious ranges
- test combination rather than monotherapy
- stratify by biomarker or genotype

## Heuristics

- Prefer approved drugs or assets with known human exposure and label information when timelines matter.
- Separate mechanistic plausibility from evidence of efficacy.
- Penalize candidates that depend on highly speculative disease biology.
- If a program was terminated or withdrawn, distinguish business failure from biological failure when possible.

## Good requests

- "Which approved drugs are most plausible for repurposing in idiopathic pulmonary fibrosis?"
- "Could this oncology asset be reused in an autoimmune indication?"
- "Rank these five drugs for repositioning against triple-negative breast cancer."

## Handoffs

- For target-first work, use `target-evidence-triage`.
- For safety translation, use `safety-pgx-brief`.
- For virtual validation against a structure, use `virtual-screening-orchestrator`.
