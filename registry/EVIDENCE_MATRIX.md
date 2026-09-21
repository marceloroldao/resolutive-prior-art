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
| RF-0002 | `marceloroldao/resolutive-routing` | Public | GitHub prerelease `v0.2.0-rc1` is tagged exactly at `17bf787d92589ad398bf9f65c1eecbbbbde8f6b1`: C++20 deterministic router, Python/C++ parity, cumulative exclusion/reroute, authenticated MA2A failure adapter, routing contract v0.2, green Python 3.10–3.13 and assertion-enabled C++ CI | `10.5281/zenodo.22235924` applies only to archived routing v0.1.0; the v0.2 GitHub release has no confirmed Zenodo DOI yet | A/B | Archive the exact `v0.2.0-rc1` tag on Zenodo, then record the new DOI without rewriting the v0.1 archive. |
| MA2A-0001 | `marceloroldao/ma2a` + prior RFC in `memoria.ia` | Public | GitHub prerelease `v0.2.0-rc1` is tagged exactly at `22846a55bc9dffdec8e8cf18aa51e3ea6756fac0`; it adds RFC v0.2, pinned routing boundary, native C++20 execution path and frozen resilient-execution contract | `10.5281/zenodo.22048589` applies only to archived MA2A v0.1.0-rc1; the v0.2 GitHub release has no confirmed Zenodo DOI yet | A/B | Archive the exact `v0.2.0-rc1` tag on Zenodo; preserve the v0.1 DOI as historical evidence. |
| MA2A-0002 | `marceloroldao/ma2a` | Public | v0.1 deterministic synchronization evidence plus v0.2 candidate `22846a55bc9dffdec8e8cf18aa51e3ea6756fac0`: real `resolutive-routing` integration, deterministic B→C→D failover, cumulative exclusions, route-vs-attempt exhaustion, assertion-enabled 17-test C++ gate and 30,000-request stress run with zero observed divergences | `10.5281/zenodo.22048589` remains the archived v0.1 MA2A record; no v0.2 DOI yet | A/B | Tag/archive the exact v0.2 candidate and preserve the stress artifact plus pinned routing SHA as release evidence. |
| MA2A-0003 | `marceloroldao/ma2a` | Public | v0.1 Ed25519 PKI/admission lineage plus v0.2 candidate `22846a55bc9dffdec8e8cf18aa51e3ea6756fac0`: signed `JobRequest`/`JobResult`/`FailureNotice`, per-target re-signing, malformed/oversized/forged-input adversarial gate, bounded TCP deadlines and `security/SECURITY_REVIEW_v0.2.md` | `10.5281/zenodo.22048589` archives only v0.1; v0.2 candidate has no DOI yet | A/B | Tag/archive the v0.2 security baseline; production channel security, PKI-bound key resolution, persistent replay protection and independent external audit remain open. |
| TRI-0001 | `marceloroldao/trivax` | Public | `0386fe8...` v0.1.0 package freeze; `f58d625...` archived v0.1.1 DOI update | `10.5281/zenodo.21989027` | A | Pin disclosure sections to exact runtime/benchmark paths and preserve archived result artifacts. |
| RI-0001 | `marceloroldao/resolutive-inference` | **Private** at audit date | `9bd6f46...` streaming edge infrastructure; `b494af9...` synthetic benchmark foundation | none | D | Publish a sufficient implementation/reproducibility baseline or ensure the public disclosure itself is enabling and archive it. |
| RC-0001 | `marceloroldao/resolutive-computing` | Public | `1122766...` initial public repository baseline; `60b0f56...` governance/licensing alignment | none | B/C | Pin benchmark scripts/results supporting coarse-to-fine claims and archive a reproducible release. |
| RT-0001 | `marceloroldao/trajectory.generator` | Public | `23e89ba...` coherence-memory universe; `bfd08d2...` exact roundtrip coverage; `ce700db...` experiment documentation | none | B | Freeze a release and quantify complete descriptor size, ambiguity and failure cases. |
| BA-0001 | `marceloroldao/bit.analyze` | Public | `1f64dca...` validation; `b5a4fe7...` overhead benchmark; `a1d7c0b...` protection buckets | none | B | Freeze/release benchmark protocol and quantify net redundancy/storage/recovery tradeoffs. |
| RP-0001 | `marceloroldao/coupled-field-vortex-model` | Public | `729e6f6...` V0.1 validation campaign; `0d3f6cd...` DOI citation update | `10.5281/zenodo.21936796` | A for the coupled-field model; C for broader Resolutive Physics | Keep broader physics claims separate; create distinct disclosures per falsifiable model/observable. |

## Audit findings

### 1. Strongest archival anchors

Public archival anchors currently include:

- Memoria.ia v0.95.1 citation/archive lineage — DOI `10.5281/zenodo.21973472`;
- TRIVAX v0.1.1 — DOI `10.5281/zenodo.21989027`;
- Coupled Field Vortex Model v0.1.0 — DOI `10.5281/zenodo.21936796`;
- MA2A v0.1.0-rc1 — DOI `10.5281/zenodo.22048589`;
- Resolutive Routing v0.1.0 — DOI `10.5281/zenodo.22235924`;
- Resolutive Prior Art Registry v0.2.0 — DOI `10.5281/zenodo.22320536`.

These DOIs identify their exact archived project/release snapshots. They do not automatically archive later development commits or later candidate releases.

### 2. Public Git history is useful but not equivalent to an archival disclosure

Trajectory Generator and Bit Analyze have useful public implementation/test history. MA2A and resolutive-routing now also have exact v0.2 candidate commits with reproducible CI evidence. These Git commits materially strengthen provenance, but they remain development evidence until each candidate is bound to an immutable tag/release and archival deposit.

### 3. Private repositories are not relied upon as public prior art

`resolutive-inference` was private when audited on 2026-08-21. Its commits can support internal provenance, but they are not treated here as public disclosure evidence. RI-0001 must therefore stand on the public specification until a sufficient implementation baseline is made public and archived.

### 4. MA2A v0.2 candidate has executable public evidence

The historical MA2A v0.1 line remains archived under DOI `10.5281/zenodo.22048589`.

The v0.2 candidate is pinned at `22846a55bc9dffdec8e8cf18aa51e3ea6756fac0`. It adds the C++20 resilient-execution path, signed execution/failure evidence, an exact routing dependency pin, adversarial transport/authentication gates, assertion-enabled Release CI and a 30,000-request deterministic stress gate with zero observed divergences.

The remaining evidentiary milestone for v0.2 is immutable tag/release + archival deposit + new DOI. The v0.1 DOI must not be reused for the v0.2 snapshot.

### 5. Resolutive-routing v0.2 candidate is pinned but not yet archived

The routing implementation candidate is pinned at `17bf787d92589ad398bf9f65c1eecbbbbde8f6b1`. It contains the C++20 routing hot path, deterministic rerouting, Python/C++ parity, authenticated MA2A failure adaptation and the v0.2 routing ownership contract.

Its historical v0.1 DOI `10.5281/zenodo.22235924` remains valid only for the archived v0.1 release.

The next evidentiary step is an immutable `v0.2.0-rc1` tag/release and a new archival DOI for that exact snapshot.

### 6. Physics requires claim-by-claim separation

The archived coupled-field vortex model is a concrete reproducible model. It must not be used as blanket evidence for unrelated cosmological, gravitational, quantum, atomic, or ontological claims. Those require separate IDs, equations, datasets, baselines, parameter accounting and falsification criteria.

## Required next archive package

For the next MA2A/routing archival update:

1. create immutable `v0.2.0-rc1` tags/releases for MA2A and resolutive-routing at the exact candidate snapshots;
2. archive those tagged snapshots on Zenodo and record their new DOIs;
3. update `releases/DOI-REGISTRY.md` only after the DOI records actually exist;
4. preserve the existing v0.1 DOI rows as historical records rather than overwriting them;
5. pin any later disclosure revision to exact source/test paths and release commits;
6. preserve EXPERIMENTAL status for claims without independent validation;
7. never rewrite archived disclosure history—use later versions or superseding IDs.
