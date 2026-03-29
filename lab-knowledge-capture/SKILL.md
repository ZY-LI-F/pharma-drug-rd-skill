---
name: lab-knowledge-capture
description: standardize experiment logging, sample and reagent traceability, and team knowledge capture using elabftw style electronic lab notebook patterns. use when the user needs a reproducible experimental record, a lab handoff checklist, or a way to turn bench activity into searchable structured knowledge.
---

# Lab Knowledge Capture

## Overview

Use this skill to convert bench work into reproducible, searchable records. It is designed for experiment logging, resource traceability, sample context, and handoff hygiene.

## Workflow

1. Identify the experiment, sample set, reagents, instruments, and operator context.
2. Separate protocol intent from what actually happened.
3. Produce a structured experiment record with attachments, metadata, and deviations.
4. Capture links to compounds, samples, storage locations, and downstream data files.
5. End with a handoff summary that another scientist can reuse.

## Output structure

### Experiment record
| field | value |
| experiment objective | |
| samples | |
| reagents | |
| protocol version | |
| deviations | |
| outputs | |
| next owner | |

### Reproducibility checklist
- exact materials and batch identifiers
- instrument or environment details
- missing metadata
- where raw data lives

### Handoff note
One short section written for the next scientist.

## Rules

- Always distinguish planned protocol from executed protocol.
- Record deviations explicitly.
- Prefer identifiers and links over prose-only notes.
- If the user asks for chemical drawing or reaction capture, note any molecule editor dependency separately.

## Good requests

- "Turn these bench notes into an ELN-ready experiment record."
- "Create a traceability template for synthesis batches and assay samples."
- "Prepare a handoff entry so another chemist can repeat this experiment."
