# DesConOps standard

Design, construct and operate as one production system: three loops, two releases, twelve steps under one contract, and four metrics that show whether it is working. This repository is the standard's definition, as JSON Schema (draft-07) and dated edition records.

- **Served:** every schema at its `$id` under `https://schemas.desconops.org/`, every edition record at its path, and [`index.json`](https://schemas.desconops.org/index.json) listing them.
- **Licence:** Apache License 2.0 (`LICENSE`, `NOTICE`).
- **Governance:** `GOVERNANCE.md`. Contributions: `CONTRIBUTING.md`.
- **Status:** draft. No version 1.0.0 schema has been released yet.

## What is here

| Path | What it is |
|---|---|
| `standard/production-system.schema.json` | The shape of the standard: loops, releases, steps and gates, the step contract, design rules, metrics, crosswalk rows, gaps and roles. |
| `editions/1.0/production-system.json` | Edition 1.0 (October 2026): the standard as its first edition states it. |
| `examples/manifest.json` | Every example and edition record, and the schema each validates with. |
| `scripts/` | The gate (`npm run check`), the served-site build (`npm run site`) and the served check (`npm run served`). |

## The production system, in one paragraph

Each step takes a keyed input, checks it against a published requirement, passes a gate held by someone with authority, and emits a record with its provenance. Twelve steps across three loops (Design, Construct, Operate), joined by two releases (issue for construction, handover), under that one contract. Four metrics, translated from software's delivery research, measure it at the gate: verified handoffs a day, design change to verified install, rework per verified install, and RFI cycle time.

## What is not here

A tool, a platform or a product. A model-data schema (IFC does that). Any one party's way of computing, scoring or deciding. The standard names the published standards that implement each step by their identifiers; it does not reference or republish them.

## Using the standard

- **Latest:** fetch a schema from its `$id`.
- **Pinned:** fetch `https://schemas.desconops.org/v/{version}/{path}` for one exact version; those bytes never change.
- **Vendored:** copy this repository at a commit or a release tag.

## Working on it

```sh
npm ci
npm run check
npm run site
```

The gate holds: canonical form, `$id` equals the served URL, closure under `https://schemas.desconops.org/`, every schema compiles, every example and edition record validates, public text clean, published versions immutable.
