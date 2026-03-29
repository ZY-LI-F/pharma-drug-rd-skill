---
name: virtual-screening-orchestrator
description: design reproducible docking and virtual screening runbooks using dockm8, easydock, and qvina style workflows. use when the user needs a consensus docking plan, a screening benchmark, or an execution-ready virtual screening specification for a protein target and compound library.
---

# Virtual Screening Orchestrator

## Overview

Use this skill to convert a target structure and a ligand library into a reproducible screening plan. It is optimized for structure-based virtual screening, consensus docking, and clear runbooks rather than ad hoc one-off docking commands.

## Workflow

1. Verify prerequisites: target structure, pocket definition, ligand library, protonation assumptions, and compute budget.
2. Decide the screening mode:
   - quick single-engine docking
   - consensus docking and rescoring
   - distributed large-library run
3. Build the run specification: software, config files, file formats, ranking metrics, and resume strategy.
4. Define quality controls: known binders, decoys, pose sanity checks, and redocking where possible.
5. Output a screening runbook and a results interpretation checklist.

## Output structure

### Screening plan
| parameter | decision |
| engine stack | |
| receptor prep | |
| ligand prep | |
| pocket definition | |
| ranking strategy | |
| compute mode | |

### QC checklist
- reference ligand or known actives
- decoys or negative controls
- protonation review
- rerun criteria

### Results interpretation
Explain how to distinguish a pose list from a genuine discovery signal.

## Engine selection guidance

- Use DockM8-style consensus workflows when robustness matters more than speed.
- Use EasyDock-style pipelines when you need automation, resumption, or distributed docking management.
- Use QVina-style acceleration when throughput is the main constraint and the setup is otherwise stable.

## Good requests

- "Design a consensus docking workflow for this kinase pocket and 50k compounds."
- "How should we prepare a reproducible docking benchmark for these known binders?"
- "Turn this protein-plus-library package into an executable screening runbook."

## Handoffs

- For structure uncertainty, use `structure-folding-planner` first.
- For ADMET filtering after hits, use `admet-property-modeler`.
