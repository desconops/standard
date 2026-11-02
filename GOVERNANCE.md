# Governance

DesConOps is an open production standard for buildings. This file says who stewards it, how it changes, and how stewardship moves.

## Steward of record

LuhTech Holdings LLC stewards the standard today. The steward holds the `desconops` GitHub organisation, the `desconops.org` domain and this repository, and reviews every change (see `.github/CODEOWNERS`).

Stewardship is designed to be handed on. The standard carries nothing that belongs to the steward: no credential, no private dependency, no reference to the steward's other systems. A transfer is a transfer of the organisation and the domain; the repository, its history, its served paths and its licence do not change.

## Roles

- **Steward.** Owns the organisation, approves releases, holds the domain.
- **Maintainers.** Review and merge changes. The `maintainers` team of the `desconops` organisation, named in `.github/CODEOWNERS`; the steward sets its membership.
- **Working group.** Anyone who proposes a change by issue or pull request. The first working-group agenda is set from the answers to the paper's three questions: which gate first, which crosswalk first, and how the four metrics are measured on real projects.

## What is in scope

The definition of the production system: its loops, releases, steps, gates, the contract every step follows, the four metrics, the crosswalks from the steps to the published standards that implement them (IFC, IDS, BCF, bSDD, ETIM, COBie and their successors), and the edition records that state the standard at a point in time.

Not in scope: any tool, platform or product; model-data schemas (IFC does that); how any one party computes, scores or decides.

## How a change lands

1. Open an issue stating the change and why. A correction to a definition, a crosswalk or a status row is a change.
2. Open a pull request. Commits carry a Developer Certificate of Origin sign-off (`git commit -s`).
3. CI must pass: canonical form, `$id` equals the served URL, closure under `https://schemas.desconops.org/`, every schema compiles, every edition record validates, public text clean, published versions immutable.
4. A maintainer reviews. The default branch takes squash merges only, linear history, no force pushes.

## Versions and editions

- A **schema** carries a semantic version. A version, once published, never changes: new content is a new version, and every published version stays served at `v/{version}/{path}`.
- An **edition record** states the standard at a date. A material change to a definition, a gate, a metric or a crosswalk is a new edition; a correction of wording is not.
- A **release** is a git tag `vX.Y.Z` on the default branch. The served site is rebuilt from the default branch on every merge.

## Licence, name and mark

Definitions, schemas, crosswalks and edition records are licensed under the Apache License, Version 2.0 (see `LICENSE` and `NOTICE`). The name "DesConOps" and the mark are held by the steward of record and transfer with stewardship (see Transfer of stewardship).

Use of the name and the mark, stated by the steward on 2026-11-02:

1. **Describing conformance is free.** Anyone may say that a tool, a project, a contract or a process implements DesConOps, or implements named steps, gates, records or metrics of it, by referring to the edition they implement (for example "implements DesConOps edition 1.0, steps 6 to 9"). No permission, fee or registration is needed.
2. **The name may not imply endorsement.** No one may use the name or the mark to state or suggest that the steward, the working group or the standard endorses, certifies, approves or ranks a product, a firm or a project. There is no certification programme; a statement such as "DesConOps-certified" is false until the steward publishes one and says so here.
3. **The name is not a product name.** The name may not be used as, or as part of, the name of a product, a service, a company, a domain or a mark, and may not be combined with another mark in a lock-up, without the steward's written agreement.
4. **The definitions are not to be altered under the name.** A modified set of definitions, gates or metrics may be published under the Apache licence, but not under the name DesConOps or a confusingly similar one; it states what it derives from and what it changed.
5. **Editions are cited by number.** A claim of conformance names the edition it rests on. Edition records are served at a fixed path and do not change after publication, so a citation stays checkable.
6. **The steward keeps the registration.** Registration of the mark, where it is registered, is held in the steward's name and is assigned to the incoming steward on transfer.

Questions about a use this policy does not cover go to the steward through this repository's issues.

## Transfer of stewardship

When a standards body or consortium takes the standard on:

1. The incoming steward is added as an owner of the `desconops` GitHub organisation; the outgoing steward removes itself.
2. The `desconops.org` registration and DNS move to the incoming steward.
3. The incoming steward sets the `maintainers` team's membership. This file and `NOTICE` are updated in one pull request that names the date of transfer; `CODEOWNERS` does not change.
4. Nothing else changes: `$id`s, served paths, versions, editions and the licence stay as they are.
