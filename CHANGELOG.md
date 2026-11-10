# Changelog

## Unreleased

- **`standard/production-system` 0.2.0.** The contract may state a fifth line, `paid`: what the gate pass is worth, to whom. Additive; edition 1.0 records still validate.
- **New: `editions/1.1/production-system.json`.** Edition 1.1, November 2026: the contract's fifth line, "the gate pass is the event work is paid on", and a logistics row in the crosswalk (GS1 EPCIS 2.0, CBV 2.0 and the GS1 identification keys at the plan, build and capture steps; partial, vendor-specific on the jobsite today). Nothing else changes from edition 1.0.

## 0.1.0 (2026-11-02)

- **New: `standard/production-system` 0.1.0 (draft).** The shape of the standard: loops, releases, steps with what crosses each gate, what it emits and who holds it; the contract every step follows; the four design rules; the four metrics with their units; the crosswalk rows from steps to published standards with a status; the three gaps; the six roles' first steps.
- **New: `editions/1.0/production-system.json`.** Edition 1.0, October 2026: the twelve steps, gates, metrics, crosswalk rows, gaps and roles as the first edition of the paper states them.
- **Repository.** Gate (`npm run check`), served-site build (`npm run site`), served check, GitHub Pages deploy, governance and contribution files, Apache-2.0 licence.
- **Governance.** The name and mark policy (GOVERNANCE.md): conformance may be described freely, endorsement may not be implied, the name is not a product name, altered definitions do not carry it, editions are cited by number, registration transfers with stewardship.
- **Served.** https://schemas.desconops.org/ live on GitHub Pages with HTTPS enforced; the served check green.
