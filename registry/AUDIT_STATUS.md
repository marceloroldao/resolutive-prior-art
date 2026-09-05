# Audit Status — v0.2.0 Release Gate

Audit date: 2026-09-05

## Current result

The v0.2.0 candidate extends the archived v0.1.0 baseline without rewriting its historical record.

New or materially strengthened disclosures in this release candidate:

- RF-0002 v0.2 — policy-first admissible routing for knowledge and compute;
- RM-0003 v0.2 — persistent concept identity and deterministic concept-relation resolution;
- RT-0002 v0.3 — information-event time, macro-event rank/unrank, and microscopic recurrent trajectory round-trip.

The v0.1.0 disclosures remain part of the registry and retain their original scope and historical publication chain.

## RM-0003 audit result

RM-0003 now has a pinned public evidence chain in `marceloroldao/memoria.ia` covering:

- stable concept identity and alias normalization;
- fail-closed contextual polysemy;
- persistence-agnostic round-trip state;
- durable Resolutive-DB persistence and restart lifecycle;
- pure-C/native resolver implementation;
- direct Python/native parity checks;
- deterministic authoritative catalog export and native BDR materialization;
- miss-only native concept activation;
- persisted-concept-to-native-HTTP end-to-end resolution.

External prior-art review found strong antecedents for broad symbolic-ID, alias, graph and disambiguation primitives. The disclosure was therefore narrowed to the specific persistent-authoritative-state -> derived-native-index -> restart -> fail-closed -> HIT/UNRESOLVED -> miss-only-native-resolution chain.

Status remains EXPERIMENTAL.

## RF-0002 audit result

RF-0002 is backed by the public `resolutive-routing` v0.1.0 prototype and archival DOI `10.5281/zenodo.22235924`.

Broad policy-first routing, scheduling, access-control and cost/latency optimization have substantial external prior art. RF-0002 is retained as a scoped Resolutive integration disclosure over memory/knowledge availability and heterogeneous compute state after admissibility filtering.

It is not currently treated as the family's strongest novelty candidate.

Status remains EXPERIMENTAL.

## RT-0002 audit result

RT-0002 now includes an operational variable-length macro-event codec plus microscopic reconstruction in the documented recurrent domain.

The evidence chain includes:

- recurrent causal core extraction;
- macrograph construction from branch states and deterministic flights;
- exact path counting for fixed public physical length;
- rank/unrank bijection over admissible macro-event sequences;
- deterministic regeneration of physical-flight lengths;
- exact microscopic node-by-node round-trip reconstruction for the tested recurrent macrograph and exhaustive small physical lengths.

The disclosure explicitly does not claim arbitrary compression beyond information-theoretic bounds, recovery from a hash alone, or invention of event time, semi-Markov processes, entropy rate, combinatorial ranking or variable-length coding in isolation.

Status remains EXPERIMENTAL because the demonstrated result is scoped to the documented recurrent domain and CI status for the newest commits was not independently exposed through the connector at audit time.

## Metadata audit

Prepared for v0.2.0:

- `CITATION.cff` -> version `0.2.0`, release date `2026-09-05`;
- `.zenodo.json` -> version `0.2.0`, publication date `2026-09-05`;
- title aligned across citation and Zenodo metadata;
- creator and ORCID aligned;
- license metadata retained as `CC-BY-NC-4.0` / `cc-by-nc-4.0`, consistent with the previous archival metadata pattern;
- disclosure versions aligned in `registry/INDEX.md`;
- companion-project DOI `10.5281/zenodo.22235924` added to the DOI registry;
- `releases/v0.2.0-MANIFEST.md` defines the exact candidate publication set and explicit non-claims.

## Release gate result

No technical-content blocker remains for creating the `v0.2.0` GitHub release.

Remaining publication actions:

1. create tag `v0.2.0` from current `main` after this audit commit;
2. create the GitHub release using the audited title/description;
3. allow Zenodo to archive that exact release snapshot;
4. record the resulting v0.2.0 DOI in `releases/DOI-REGISTRY.md` and README;
5. keep the v0.1.0 DOI mapping unchanged as historical provenance.

## Legal / scope note

This is a technical defensive-publication registry, not a patent filing or legal opinion. Publication can affect patent rights depending on jurisdiction and timing. The registry deliberately distinguishes implementation evidence from novelty, patentability, freedom to operate and scientific validation.
