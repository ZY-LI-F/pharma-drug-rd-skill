---
name: admet-property-modeler
description: design qsar, property prediction, and admet modeling workflows for lead optimization using chemprop, deepchem, or torchdrug style libraries. use when the user needs a reproducible plan for molecular property prediction, toxicity classification, permeability or exposure proxies, or model-based triage of leads.
---

# ADMET Property Modeler

## Overview

Plan data-driven property modeling and lead triage. This skill is best for ADMET-like prediction work where the user needs to decide which modeling stack fits the dataset, how to split data correctly, and how to turn predictions into medicinal-chemistry decisions.

## Workflow

1. Define the prediction task: classification, regression, multitask, or uncertainty-aware ranking.
2. Inventory the data: assay endpoint, units, leakage risks, scaffold diversity, and sample size.
3. Choose the modeling stack:
   - Chemprop for strong molecule property baselines with message passing neural networks
   - DeepChem for broad drug-discovery ML workflows and tutorials
   - TorchDrug for graph-first research prototyping and richer graph tasks
4. Specify data split, metrics, calibration, and applicability domain checks.
5. Convert the model output into lead-optimization actions.

## Output contract

### Modeling brief
| question | answer |
| endpoint | |
| dataset size | |
| split strategy | |
| baseline | |
| primary metric | |
| deployment form | |

### Risk controls
- leakage checks
- scaffold split or time split
- class imbalance handling
- uncertainty or calibration notes

### Decision layer
Translate predictions into chemist-friendly actions such as keep, deprioritize, redesign, or synthesize analogs around a motif.

## Rules

- Never present an AUC or RMSE without explaining dataset split and leakage risk.
- Prefer simple baselines before complex stacks when data is small.
- Separate model confidence from biological confidence.

## Good requests

- "Design an ADMET triage workflow for 20k compounds with sparse assay coverage."
- "Should we use Chemprop or DeepChem for this permeability endpoint?"
- "Turn this Tox21-like dataset into a reproducible modeling plan."
