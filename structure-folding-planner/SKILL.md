---
name: structure-folding-planner
description: plan protein or complex structure preparation workflows for discovery teams using openfold or paddlehelix style toolchains. use when the user needs a structure-first plan for target modeling, mutant comparison, pocket analysis readiness, or downstream docking preparation.
---

# Structure Folding Planner

## Overview

Translate a biological target question into a practical structure-preparation plan. This skill is for structure-first discovery work: target modeling, mutant comparisons, structure confidence review, and preparing inputs for docking or design.

## Default workflow

1. Identify the protein, construct, species, mutations, ligands, and oligomeric context.
2. Decide whether an experimental structure already exists or a predicted structure is needed.
3. Choose a modeling path:
   - OpenFold-style open AlphaFold2 reproduction for trainable or reproducible protein structure prediction
   - PaddleHelix / HelixFold path when broader biocomputing workflows or protein-related tasks are in scope
4. Produce an execution plan covering inputs, compute assumptions, expected outputs, and model-confidence review.
5. End with how the structure will be consumed next: pocket analysis, docking, mutational analysis, or design.

## Output contract

### Modeling decision
- existing structure reuse
- predicted monomer
- predicted complex or multimer
- stop because the question is not structure-limited

### Run plan
| item | choice |
| target construct | |
| sequence source | |
| mutations | |
| modeling engine | |
| expected output files | |
| downstream consumer | |

### Confidence review
Comment on domain confidence, disordered regions, binding-site uncertainty, and mutations near the pocket.

## Rules

- Treat a predicted structure as a hypothesis, not truth.
- State clearly when pocket geometry may be too uncertain for docking.
- If the user needs ranking of compounds, hand off to `virtual-screening-orchestrator`.
- If the user needs generative design, hand off to `de-novo-molecule-generator`.

## Good requests

- "Plan a structure workflow for this kinase mutant before docking."
- "Should we use an experimental structure or predict one first?"
- "Prepare a fold-and-pocket assessment plan for this membrane target."
