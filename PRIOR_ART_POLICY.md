# Prior Art Publication Policy

## Purpose

This repository is the canonical public registry for technical disclosures in the Resolutive Technology family. Its purpose is to preserve dated, versioned, technically meaningful disclosures that can be independently read, implemented, tested, and cited.

## Core rule

A disclosure must describe a technical mechanism, not merely an aspiration, product claim, or broad idea.

Each disclosure SHOULD contain:

1. a clearly stated technical problem;
2. the proposed mechanism or architecture;
3. definitions and assumptions;
4. algorithm, state machine, equations, protocol structure, or pseudocode where applicable;
5. at least one concrete worked example or reference implementation when feasible;
6. reproducibility or test evidence where a claim is empirical;
7. known limitations and unresolved questions;
8. links to implementation repositories, commits, releases, datasets, and DOI records where available.

## Evidence status

Every disclosure MUST use one of these statuses:

- `DRAFT` — incomplete and not intended as a stable disclosure.
- `EXPERIMENTAL` — mechanism is specified and under active testing.
- `VALIDATED` — stated technical behavior has reproducible supporting evidence within the defined scope.
- `PUBLISHED` — frozen public disclosure included in a versioned release and, when applicable, an archival DOI deposit.
- `SUPERSEDED` — replaced by a later disclosure; historical record is retained.
- `RETRACTED` — material technical error identified; historical record is retained with reason.

A status describes evidence maturity, not commercial readiness and not universal scientific truth.

## Identifier namespaces

- `RM-xxxx` — Resolutive Memory / Memoria.ia
- `MA2A-xxxx` — Memoria.ia Agent-to-Agent Protocol
- `TRI-xxxx` — TRIVAX
- `RI-xxxx` — Resolutive Inference
- `RC-xxxx` — Resolutive Computing
- `RT-xxxx` — Resolutive Trajectory / reversible trajectory systems
- `BA-xxxx` — Bit Analysis / hierarchical relation analysis
- `RP-xxxx` — Resolutive Physics hypotheses and models

Identifiers are never reused.

## Publication chain

Preferred chain:

`Disclosure -> Specification -> Algorithm/Protocol -> Evidence -> Implementation -> Commit -> Release -> Archival deposit/DOI`

A Git commit provides repository history; an archival release provides a stable citation object. Neither substitutes for a technically enabling disclosure.

## Amendments

Published disclosures are not silently rewritten to change their technical substance. Material changes create a new version or a new disclosure ID. Corrections MUST be recorded in history.

## Security and secrets

Never publish private keys, production credentials, customer data, operational secrets, or other sensitive infrastructure material. Defensive disclosure concerns technical mechanisms, not secrets required to operate production systems securely.

## Legal note

This repository is a technical publication registry, not a patent filing and not legal advice. Public disclosure may affect patent rights, including the author's own rights, depending on jurisdiction and timing. Significant releases should be reviewed for legal and licensing implications before archival publication.
