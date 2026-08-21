# Disclosure Timeline

Chronological registry of public technical disclosures in the Resolutive Technology family.

Only concrete public disclosures are entered here. Draft placeholders belong in `registry/INDEX.md` until a specification exists.

| Date | ID | Version | Status | Release | DOI | Notes |
|---|---|---:|---|---|---|---|
| 2026-08-21 | RM-0001 | 0.1 | EXPERIMENTAL | pending immutable registry release | Memoria.ia project record 10.5281/zenodo.21973472 | Core resolutive-memory mechanism disclosed; O(1) claim explicitly limited to known-address resolution. |
| 2026-08-21 | RM-0002 | 0.1 | EXPERIMENTAL | pending immutable registry release | — | Trajectory descriptor architecture disclosed; hash treated as verifier, not standalone reversible storage. |
| 2026-08-21 | MA2A-0001 | 0.1 | EXPERIMENTAL | pending immutable registry release | — | L1/L2/L3 state-synchronization architecture disclosed; LLM semantics remain edge-side and optional. |
| 2026-08-21 | MA2A-0002 | 0.1 | EXPERIMENTAL | pending immutable registry release | — | Versioned trajectory-delta synchronization and deterministic conflict classes disclosed. |
| 2026-08-21 | MA2A-0003 | 0.1 | EXPERIMENTAL | pending immutable registry release | — | Organization-rooted Ed25519 PKI, delegated device credentials, challenge-response admission, and revocation/licensing-status separation disclosed. |

## Rules

1. Dates use ISO 8601 (`YYYY-MM-DD`).
2. Historical entries are never deleted to conceal supersession or retraction.
3. A `PUBLISHED` entry should reference an immutable release/tag and, when available, an archival DOI.
4. A later technical improvement receives a new version or disclosure ID rather than silently changing the historical record.
5. `EXPERIMENTAL` records may document concrete mechanisms before a frozen archival release, but must state unresolved evidence and reproducibility gaps.
