# Pharma Drug R&D Skill Suite

A public collection of reusable ChatGPT skills for computational and digital drug research and development.

This repository packages **workflow-oriented skills**, not third-party model weights or upstream codebases. The goal is to provide reusable skill specifications that help ChatGPT support common tasks across target discovery, repurposing, safety review, structure preparation, virtual screening, ADMET modeling, de novo design, clinical study operations, and lab knowledge capture.

## Why this repository exists

Drug R&D work is fragmented across evidence synthesis, structure-based design, molecular machine learning, clinical operations, and experimental record keeping. This repository turns those recurring workflows into reusable ChatGPT skills so teams can:

- standardize reasoning and deliverable formats
- shorten setup time for repeated analysis tasks
- make project handoffs more consistent
- connect open-source drug discovery tooling with clear task-oriented prompts

## Scope

This repository currently focuses on:

- target discovery and validation triage
- repurposing hypothesis screening
- safety, pharmacogenomics, and labeling review
- protein structure planning
- virtual screening orchestration
- ADMET and property modeling
- target-conditioned de novo molecule design planning
- clinical study operations planning
- laboratory knowledge capture and reproducibility

This repository does **not** currently provide production-ready wet-lab protocols, regulated GxP workflows, validated submission documents, or bundled copies of upstream project code.

## Repository structure

```text
.
├── README.md
├── README_CN.md
├── OPEN_SOURCE_SOURCES.md
├── target-evidence-triage/
├── repurposing-hypothesis-screen/
├── safety-pgx-brief/
├── structure-folding-planner/
├── virtual-screening-orchestrator/
├── admet-property-modeler/
├── de-novo-molecule-generator/
├── clinical-study-ops/
└── lab-knowledge-capture/
```

## Included skills

| Stage | Skill | What it does |
|---|---|---|
| Target discovery / validation | `target-evidence-triage` | ranks targets using disease, mechanism, druggability, and translational evidence |
| Repurposing | `repurposing-hypothesis-screen` | screens approved or existing assets for indication expansion |
| Safety translation | `safety-pgx-brief` | combines ADR, DDI, PGx, and labeling risks into a decision brief |
| Structure preparation | `structure-folding-planner` | plans target structure modeling and downstream docking readiness |
| Virtual screening | `virtual-screening-orchestrator` | specifies reproducible docking and screening runbooks |
| ADMET / QSAR | `admet-property-modeler` | plans molecular property and toxicity modeling workflows |
| De novo design | `de-novo-molecule-generator` | defines constraint-driven generative chemistry campaigns |
| Clinical operations | `clinical-study-ops` | turns study concepts into EDC and data-management setup plans |
| Lab operations | `lab-knowledge-capture` | standardizes experiment records, traceability, and handoffs |

## Referenced open-source projects

The following public projects informed the task boundaries, workflow patterns, and project selection in this repository. Their code is **not vendored here** unless explicitly stated in the future.

| Project | Repository | How it informs this repository |
|---|---|---|
| DrugClaw | `https://github.com/DrugClaw/DrugClaw` | evidence synthesis, target intelligence, literature, compound triage, and docking-oriented AI assistant concepts |
| OpenFold | `https://github.com/aqlaboratory/openfold` | protein structure prediction planning and model-readiness workflows |
| PaddleHelix | `https://github.com/PaddlePaddle/PaddleHelix` | broader bio-computing coverage across structure, DTI, molecular generation, and ADMET-related tasks |
| DockM8 | `https://github.com/DrugBud-Suite/DockM8` | consensus docking and virtual screening workflow design |
| EasyDock | `https://github.com/ci-lab-cz/easydock` | automated docking pipelines and distributed execution patterns |
| Chemprop | `https://github.com/chemprop/chemprop` | message-passing neural network workflows for molecular property prediction |
| DeepChem | `https://github.com/deepchem/deepchem` | general-purpose open-source deep learning workflows for drug discovery and chemistry |
| TorchDrug | `https://github.com/DeepGraphLearning/torchdrug` | graph learning workflows for drug discovery and molecular ML research |
| DrugGEN | `https://github.com/HUBioDataLab/DrugGEN` | target-conditioned de novo molecule generation campaign design |
| OpenClinica | `https://github.com/OpenClinica/OpenClinica` | open clinical EDC/CDM workflow concepts for study operations |
| eLabFTW | `https://github.com/elabftw/elabftw` | electronic lab notebook, traceability, and experiment knowledge capture patterns |
| AI4Green | `https://github.com/AI4Green/AI4Green` | chemistry-oriented ELN and sustainability-aware laboratory workflow ideas |

## Attribution and citation

If you use this repository in research or internal enablement work:

1. cite or acknowledge the specific upstream open-source projects that informed your workflow;
2. do not imply endorsement by those upstream maintainers;
3. verify license compatibility before copying code, models, or assets from upstream repositories.

See [`OPEN_SOURCE_SOURCES.md`](./OPEN_SOURCE_SOURCES.md) for the provenance summary.

## How to use

### 1. Browse the repository
Open the skill folder that matches the stage of your program.

### 2. Read the skill specification
Each skill exposes its own `SKILL.md` with:
- trigger conditions
- workflow steps
- output structure
- handoff rules to other skills

### 3. Upload or adapt the skill
Use the skill content as a reusable workflow specification in ChatGPT or adapt it for your internal deployment process.

## Suggested skill bundles

- **Early discovery**: `target-evidence-triage` + `repurposing-hypothesis-screen` + `safety-pgx-brief`
- **Structure-based design**: `structure-folding-planner` + `virtual-screening-orchestrator` + `admet-property-modeler`
- **Generative design**: `de-novo-molecule-generator` + `virtual-screening-orchestrator` + `admet-property-modeler`
- **Translation and execution**: `clinical-study-ops` + `lab-knowledge-capture`

## Design principles

- **Workflow-first**: optimize for repeatable decision workflows rather than one-off prompts.
- **Source-aware**: keep upstream project provenance visible.
- **Non-vendoring by default**: avoid copying third-party code into this repository unless licensing and maintenance are explicit.
- **Composable skills**: each skill should stand alone but also hand off cleanly to adjacent stages.
- **Transparent boundaries**: separate evidence generation, model planning, and operational execution.

## Limitations

This version does not yet include dedicated skills for:

- CMC process development
- GMP manufacturing execution
- eCTD submission authoring
- enterprise-specific QMS integrations

Those areas usually require organization-specific SOPs, validated templates, and regulated systems.

## Contributing

Issues and pull requests are welcome for:

- better skill wording
- improved stage coverage
- more precise upstream attribution
- new open-source project mappings
- additional deployment metadata such as `agents/openai.yaml`

When contributing, please keep provenance explicit and avoid adding third-party code or assets without confirming license compatibility.

## License

A repository-wide license file has not yet been added. Add a project license before reusing this repository as a general redistribution artifact.
