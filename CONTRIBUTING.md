# Contributing

Thanks for contributing to **Pharma Drug R&D Skill Suite**.

This repository collects reusable ChatGPT skills for computational and digital drug R&D. Contributions are welcome, especially when they improve skill quality, provenance clarity, and stage coverage.

## What to contribute

Good contributions include:

- clearer or more robust `SKILL.md` instructions
- new skills for adjacent drug R&D stages
- better open-source project mapping and attribution
- documentation improvements
- packaging metadata such as `agents/openai.yaml`

## Before you contribute

Please make sure your contribution:

1. keeps upstream project provenance explicit;
2. does not vendor third-party code, models, weights, or assets unless license compatibility is verified;
3. does not imply endorsement by upstream projects;
4. states assumptions and workflow boundaries clearly.

## Skill design expectations

When adding or editing a skill:

- keep the frontmatter `name` and `description` lowercase;
- make the description specific enough to act as a trigger condition;
- prefer workflow-oriented instructions over vague advice;
- define expected inputs, outputs, and handoff rules;
- separate planning guidance from claims of experimental validation.

## Recommended skill structure

```text
skill-name/
├── SKILL.md
├── references/
├── scripts/
└── agents/
```

Not every skill needs all subfolders, but each addition should stay lightweight and easy to audit.

## Attribution rules

If your contribution is inspired by an upstream open-source project:

- add or update the project in `README.md` under the referenced project list;
- update `OPEN_SOURCE_SOURCES.md` if the provenance scope changes;
- mention the upstream project and repository in your pull request description.

## Pull request checklist

Before opening a pull request, verify that:

- the skill is clearly scoped;
- the repository documentation still matches the actual contents;
- no copyrighted third-party materials were copied in without permission;
- any new source mapping is accurate and visible.

## Reporting issues

When filing an issue, include:

- the skill name
- the stage of drug R&D involved
- the expected behavior
- the actual behavior or gap
- any relevant upstream project or source context

## Code of conduct

Please be respectful, transparent about sources, and conservative about biomedical claims. This repository is intended for planning and enablement workflows, not for overstating scientific or regulatory conclusions.
