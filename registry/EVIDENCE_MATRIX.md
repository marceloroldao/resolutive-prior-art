# Cross-Repository Evidence Matrix

This matrix links each Resolutive disclosure to public or private implementation evidence. It records documentary strength; it does not establish patentability, scientific validity, or freedom to operate.

## Evidence levels

- **A — Archived public baseline:** public repository + pinned commit/release + reproducibility material + archival DOI.
- **B — Public reproducible development evidence:** public repository + pinned implementation/test/benchmark commits, but no disclosure-specific archival DOI yet.
- **C — Public specification / partial implementation:** public technical disclosure exists, but implementation freeze, security validation, or reproducibility package is incomplete.
- **D — Non-public implementation dependency:** technical disclosure may be public, but the primary implementation repository is private or otherwise unavailable as public prior-art evidence.

| Disclosure | Primary repository/evidence | Visibility | Pinned evidence | DOI/archive | Level | Main gap before PUBLISHED |
|---|---|---|---|---|---|---|
| RM-0001 | `marceloroldao/memoria.ia` | Public | `c1585f6...` stable v0.95.0 line; `263a731...` current docs lineage | `10.5281/zenodo.21973472` (v0.95.1 citation record) | A/B | Pin exact core source/test paths for each normative RM primitive and archive this registry disclosure. |
| RM-0002 | `marceloroldao/trajectory.generator` + `memoria.ia` | Public | trajectory exact-roundtrip/test line including `bfd08d2...` | none specific | B | Prove reconstruction contract with all descriptor/side-information bits accounted for; do not infer compression. |
| MA2A-0001 | `marceloroldao/ma2a` + prior RFC in `memoria.ia` | Public | MA2A bootstrap branch; `b2fef4b...` prior RFC lineage | none specific | B/C | Freeze v0.1 release/tag and add wire-level interoperability tests. |
| MA2A-0002 | `marceloroldao/ma2a` | Public | deterministic conflict resolver + convergence/replay/scope/stale tests on `bootstrap/v0.1-dev` | none | B | Obtain CI evidence, freeze policy version and archive release. |
| MA2A-0003 | `marceloroldao/ma2a` | Public | `2889e63...` Ed25519 certificate/handshake reference; `ba21c07...` negative auth tests | none | B/C | Complete CI/security review, add tampered-certificate/delegation tests, freeze release and archive DOI. |
| TRI-0001 | `marceloroldao/trivax` | Public | `0386fe8...` v0.1.0 package freeze; `f58d625...` archived v0.1.1 DOI update | `10.5281/zenodo.21989027` | A | Pin disclosure sections to exact runtime/benchmark paths and preserve archived result artifacts. |
| RI-0001 | `marceloroldao/resolutive-inference` | **Private** at audit date | `9bd6f46...` streaming edge infrastructure; `b494af9...` synthetic benchmark foundation | none | D | Publish a sufficient implementation/reproducibility baseline or ensure the public disclosure itself is enabling and archive it. |
| RC-0001 | `marceloroldao/resolutive-computing` | Public | `1122766...` initial public repository baseline; `60b0f56...` governance/licensing alignment | none | B/C | Pin benchmark scripts/results supporting coarse-to-fine claims and archive a reproducible release. |
| RT-0001 | `marceloroldao/trajectory.generator` | Public | `23e89ba...` coherence-memory universe; `bfd08d2...` exact roundtrip coverage; `ce700db...` experiment documentation | none | B | Freeze a release and quantify complete descriptor size, ambiguity and failure cases. |
| BA-0001 | `marceloroldao/bit.analyze` | Public | `1f64dca...` validation; `b5a4fe7...` overhead benchmark; `a1d7c0b...` protection buckets | none | B | Freeze/release benchmark protocol and quantify net redundancy/storage/recovery tradeoffs. |
| RP-0001 | `marceloroldao/coupled-field-vortex-model` | Public | `729e6f6...` V0.1 validation campaign; `0d3f6cd...` DOI citation update | `10.5281/zenodo.21936796` | A for the coupled-field model; C for broader Resolutive Physics | Keep broader physics claims separate; create distinct disclosures per falsifiable model/observable. |

## Audit findings

### 1. Strongest archival anchors

At this audit date, the strongest public archival anchors are:

- Memoria.ia v0.95.1 citation/archive lineage — DOI `10.5281/zenodo.21973472`;
- TRIVAX v0.1.1 — DOI `10.5281/zenodo.21989027`;
- Coupled Field Vortex Model v0.1.0 — DOI `10.5281/zenodo.21936796`.

These DOIs archive project/release evidence. They do not automatically archive every later disclosure in this registry; a `resolutive-prior-art` release should receive its own archival record.

### 2. Public Git history is useful but not equivalent to an archival disclosure

Trajectory Generator, Bit Analyze and MA2A now have useful public implementation/test history. Their evidence strength will improve materially once release tags and immutable archives bind implementation, tests, documentation and disclosure to the same snapshot.

### 3. Private repositories are not relied upon as public prior art

`resolutive-inference` was private when audited on 2026-08-21. Its commits can support internal provenance, but they are not treated here as public disclosure evidence. RI-0001 must therefore stand on the public specification until a sufficient implementation baseline is made public and archived.

### 4. MA2A now has executable public evidence

The dedicated public `marceloroldao/ma2a` repository now contains the protocol draft, a deterministic conflict-resolution reference implementation, an Ed25519 organization/device certificate model, challenge-response authentication, and negative tests. The remaining milestone is not more architecture prose: it is CI/security evidence, interoperability testing, release freeze and archival DOI.

### 5. Physics requires claim-by-claim separation

The archived coupled-field vortex model is a concrete reproducible model. It must not be used as blanket evidence for unrelated cosmological, gravitational, quantum, atomic, or ontological claims. Those require separate IDs, equations, datasets, baselines, parameter accounting and falsification criteria.

## Required next archive package

Before `resolutive-prior-art` v0.1 is marked PUBLISHED:

1. pin all disclosure files to this repository commit/tag;
2. add exact source/test paths where available;
3. run a link/reference consistency check;
4. preserve EXPERIMENTAL status for claims without independent validation;
5. create an immutable GitHub release/tag;
6. archive the release on Zenodo and record its DOI in `releases/DOI-REGISTRY.md`;
7. never rewrite the archived v0.1 disclosure history—use later versions or superseding IDs.
