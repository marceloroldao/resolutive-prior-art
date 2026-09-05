# Resolutive Family Snapshot — 2026-09-05

This snapshot records post-v0.1.0 technical evolution across the Resolutive repositories and identifies what should enter the next defensive-publication release.

## New disclosure candidates promoted

### RM-0003 — Persistent Concept Identity and Deterministic Concept-Relation Resolution

Source repository: `marceloroldao/memoria.ia`.

Key public evolution:

- stable concept IDs distinct from surface text;
- alias normalization and namespace isolation;
- contextual polysemy with fail-closed ambiguity;
- bounded relation-path traversal with provenance;
- deterministic authoritative concept-catalog export;
- durable native concept state in Resolutive-DB;
- Python/native parity gating;
- miss-only native concept-resolution activation;
- persisted concept -> native HTTP resolution end-to-end evidence.

Current public integration baseline: `4f9ac9440c56855266ab3d1acd853b0706dee646`.

### RF-0002 — Policy-First Admissible Routing for Knowledge and Compute

Source repository: `marceloroldao/resolutive-routing`.

The routing layer is now an independent public prototype with archival DOI `10.5281/zenodo.22235924`. It separates knowledge location from compute suitability and enforces privacy/policy admissibility before optimization across knowledge, model capability, CPU/GPU/NPU resources, load, latency, reputation, cost/energy and contribution balances.

### RT-0002 — Information-Event Time and Recurrent Causal Trajectory Compression

Source repository: `marceloroldao/trajectory.generator`.

Post-v0.1 trajectory work now distinguishes physical transition time from entropy-bearing branch-event time. A recurrent causal graph can be reduced to variable-length deterministic flights between branch states while preserving the asymptotic growth factor of the admissible trajectory language. This is explicitly limited to constrained admissible families and does not claim arbitrary-data compression beyond information-theoretic bounds.

## Evidence-only updates

### Resolutive-DB

No new independent disclosure is created in this snapshot. Relevant evolution is treated as supporting evidence for RM-0003:

- atomic Android C ABI and recovery contract;
- torn-tail recovery testing;
- use as durable backing for native concept-state materialization in Memoria.ia.

The database remains an implementation substrate unless a separately distinct storage/recovery mechanism is isolated and surveyed.

### MA2A

The MA2A repository contains the RM-MA2A route-transfer bridge and later documentation defining the Memoria.ia/MA2A integration boundary. This strengthens evidence around MA2A-0002 and the narrow RM<->MA2A claim chart but does not require a new protocol disclosure yet.

Relevant commits include:

- `6bfd73d1873826bd2e8db03cd3b3a0aceafde2c0` — RM-MA2A route synchronization bridge;
- `a8011261a78c8e030cd2bdd78e7e356d6f728d0c` — learned-route transfer interoperability test;
- `f3df9832d0230bc8ab02bc957c2430b1952ddd2b` — Memoria.ia to MA2A integration boundary.

## Repositories reviewed but not promoted in this snapshot

- `resolutive-computing` — retain RC-0001 pending a newly isolated post-v0.1 mechanism with reproducible evidence.
- `resolutive-inference` — retain RI-0001 pending a newly isolated mechanism distinct from existing inference disclosure.
- `trivax` — retain TRI-0001; no snapshot-driven promotion here.
- `bit.analyze` — retain BA-0001; repository is currently private and any new defensive disclosure should be intentionally reviewed before publication.
- `off.ia` — product/integration repository, currently private; do not automatically disclose product-specific internals.
- `memoria.ia.server` — deployment/management layer, currently private; no defensive publication without an intentionally isolated technical mechanism.

## v0.2 publication intent

The next archival release should preserve v0.1.0 unchanged and add, at minimum:

- RF-0002;
- RM-0003;
- RT-0002;
- updated evidence links for MA2A and Resolutive-DB;
- updated external-prior-art surveys for the new mechanisms before changing their status from EXPERIMENTAL.

A v0.2 release should be created only after metadata consistency, external-prior-art review and exact source-commit pinning are complete.
