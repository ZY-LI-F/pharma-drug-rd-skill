---
name: de-novo-molecule-generator
description: plan target-conditioned de novo design workflows using druggen style generative models and downstream medicinal chemistry guardrails. use when the user wants to generate new candidate molecules for a target, define generation constraints, or turn a target profile into a design campaign brief.
---

# De Novo Molecule Generator

## Overview

Turn a target profile into a controlled de novo design campaign. This skill is for generative molecule ideation, not for claiming that generated compounds are validated hits.

## Workflow

1. Normalize the target, design objective, and hard constraints.
2. Separate must-have constraints from soft optimization goals.
3. Choose a generation mode:
   - target-conditioned de novo design
   - scaffold-aware exploration
   - novelty-biased exploration
4. Specify post-generation filters: synthetic plausibility proxy, ADMET proxy, docking follow-up, and diversity clustering.
5. Output a campaign brief, not just a list of molecules.

## Output contract

### Campaign brief
| field | value |
| target | |
| objective | |
| hard constraints | |
| soft objectives | |
| diversity policy | |
| follow-up assays | |

### Post-generation filter stack
- medicinal chemistry sanity checks
- novelty and diversity filters
- ADMET triage
- docking or structural follow-up

### Success criteria
Define what would count as a useful generation round.

## Rules

- State clearly that generated molecules are hypotheses.
- Do not confuse novelty with quality.
- Require at least one downstream validation route such as docking, activity prediction, or synthesis review.
- If the user lacks a target or objective, push back and ask for a better design brief.

## Good requests

- "Plan a target-conditioned de novo design campaign for AKT1 with oral-drug-like constraints."
- "Generate the constraint sheet and evaluation protocol for a novelty-biased design round."
- "How should we post-filter de novo molecules before synthesis?"
