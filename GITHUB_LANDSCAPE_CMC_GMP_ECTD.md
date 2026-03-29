# GitHub Landscape for CMC / GMP / eCTD Skills

## Bottom line

A search of public GitHub repositories did **not** identify a mature, reusable ChatGPT `SKILL.md`-style skill dedicated specifically to pharmaceutical **CMC**, **GMP/cGMP**, or **eCTD publishing**.

What exists publicly is mostly one of the following:

1. **adjacent tooling** rather than ChatGPT skills;
2. **submission examples** rather than reusable workflow instructions;
3. **quality systems or PLM platforms** rather than regulatory reasoning assets.

## Public repositories worth noting

### eCTD-adjacent
- `RConsortium/submissions-pilot3-adam-to-fda`
  - useful as an example eCTD-like package structure for FDA-related submissions
  - not a reusable ChatGPT skill
- public eCTD validator/publisher searches
  - results are fragmented and often proprietary, inactive, or not focused on drug-registration workflows

### GMP / quality-system-adjacent
- `dromation/open-eqms`
  - enterprise quality management system concept
  - not a GMP interpretation skill
- `C-realize/OpenQMS`
  - lightweight quality management platform
  - not an FDA/NMPA rules engine or skill
- `becpg/becpg-community`
  - product lifecycle and quality/regulatory workflows
  - strong adjacent platform, but not a submission-readiness skill

## Design decision for this repository

Because a trustworthy public GitHub skill set was not found, the skills added in this repository are grounded primarily in:

- FDA official regulations, guidances, and technical conformance resources
- NMPA / CDE official regulations, technical specifications, and guidance documents

GitHub projects are treated only as **ecosystem references** and **implementation inspiration**, not as normative regulatory sources.
