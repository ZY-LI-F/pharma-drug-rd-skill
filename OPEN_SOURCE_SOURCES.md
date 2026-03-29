# Open Source Provenance

This repository assembles reusable ChatGPT skills for drug research and development.
It does **not** bundle third-party project code. Instead, each skill is a workflow specification inspired by public open-source projects and their task boundaries.

## Primary source groups

### DrugClaw-derived evidence skills
Used for:
- target evidence triage
- repurposing hypothesis screening
- safety and PGx briefing

Why:
DrugClaw is strongest on evidence synthesis across drug targets, mechanisms, adverse drug reactions, drug-drug interactions, labeling, pharmacogenomics, and repurposing-oriented biomedical reasoning.

Mapped skills:
- `target-evidence-triage`
- `repurposing-hypothesis-screen`
- `safety-pgx-brief`

### Structure and modeling sources
Used for:
- protein and complex structure planning

Representative public projects:
- OpenFold
- PaddleHelix / HelixFold

Mapped skill:
- `structure-folding-planner`

### Virtual screening sources
Used for:
- docking and screening workflow design

Representative public projects:
- DockM8
- EasyDock
- QVina

Mapped skill:
- `virtual-screening-orchestrator`

### ADMET and molecular ML sources
Used for:
- property prediction
- QSAR planning
- lead triage

Representative public projects:
- Chemprop
- DeepChem
- TorchDrug

Mapped skill:
- `admet-property-modeler`

### Generative chemistry sources
Used for:
- target-conditioned de novo design planning

Representative public projects:
- DrugGEN

Mapped skill:
- `de-novo-molecule-generator`

### Clinical and laboratory operations sources
Used for:
- clinical study setup planning
- experiment logging and traceability

Representative public projects:
- OpenClinica
- eLabFTW
- AI4Green

Mapped skills:
- `clinical-study-ops`
- `lab-knowledge-capture`

## Important boundary

These skills are planning and reasoning assets for ChatGPT. They are not substitutes for validated wet-lab protocols, regulated GxP systems, or production-grade submission workflows.

## Not covered in this version

This version does not include standalone skills for:
- CMC process development
- GMP manufacturing execution
- eCTD submission authoring
- enterprise-specific QMS workflows

Those areas usually depend on internal SOPs, templates, and regulated systems rather than general-purpose public GitHub projects.
