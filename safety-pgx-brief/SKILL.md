---
name: safety-pgx-brief
description: generate a translational safety brief that combines adverse reactions, drug-drug interactions, pharmacogenomics, labeling, and clinical caveats. use when the user needs early safety triage, a genotype-aware risk note, or a concise briefing before advancing a candidate or repurposing hypothesis.
---

# Safety PGx Brief

## Overview

Build a cross-source safety narrative for a drug, candidate list, or mechanism class. This skill is designed for translational risk reviews where adverse reactions, DDI, pharmacogenomics, and label constraints must be seen together.

## Workflow

1. Normalize the drug names and aliases.
2. Separate known safety evidence into ADR, DDI, PGx, labeling, and clinical-use constraints.
3. Highlight population-specific risks such as genotype, organ impairment, or class effects.
4. Produce a decision-oriented brief with risk severity, confidence, and mitigation ideas.

## Output structure

### Executive risk call
One paragraph with red, yellow, or green status.

### Risk matrix
| risk domain | finding | who is affected | evidence strength | mitigation |

### PGx section
- variants or genotype context
- expected exposure, efficacy, or toxicity impact
- whether the issue is mandatory screening, optional stratification, or exploratory

### Decision section
- continue
- continue with stratification
- continue with monitoring
- pause pending new data

## Rules

- Never merge all safety evidence into one undifferentiated paragraph.
- Separate label-derived facts from literature-derived hypotheses.
- If the signal is sparse or spontaneous-report-driven, say that explicitly.
- If multiple drugs are compared, make the comparison symmetrical.

## Good requests

- "Prepare a genotype-aware safety brief for thiopurines."
- "What are the key DDI and ADR liabilities for adding this drug into a combination regimen?"
- "Which candidate is safer to carry into translational work for elderly patients?"

## Handoffs

- If the user asks whether the safety tradeoff is worth a new indication, pair this with `repurposing-hypothesis-screen`.
- If the user asks how safety should influence target selection, pair this with `target-evidence-triage`.
