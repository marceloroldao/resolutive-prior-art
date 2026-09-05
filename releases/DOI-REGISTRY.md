# DOI Registry

This file maps repository releases and individual technical disclosures to archival DOI records.

| Repository / Release | Date | DOI | Related disclosure(s) | Notes |
|---|---|---|---|---|
| Memoria.ia v0.95.1 | 2026-08-17 | 10.5281/zenodo.21973472 | RM-0001 lineage | Existing archived project/release record; does not automatically archive later prior-art text. |
| TRIVAX v0.1.1 | 2026-08 | 10.5281/zenodo.21989027 | TRI-0001 | Archived public experimental baseline. |
| Coupled Field Vortex Model v0.1.0 | 2026-08-14 | 10.5281/zenodo.21936796 | RP-0001 related model evidence | Applies to the concrete coupled-field model, not to broader Resolutive Physics claims. |
| MA2A v0.1.0-rc1 | 2026-08-21 | 10.5281/zenodo.22048589 | MA2A-0001, MA2A-0002, MA2A-0003 | First public archived MA2A release candidate; DOI applies to the archived release snapshot, not later `main` commits. |
| Resolutive Prior Art Registry v0.1.0 | 2026-08-22 | 10.5281/zenodo.22055552 | RF/RM/MA2A/TRI/RI/RC/RT/BA/RP | First archival defensive-publication release of the registry. RF-0001 is the cross-family foundation for the computing architecture. |
| Resolutive Routing v0.1.0 | 2026-09-01 | 10.5281/zenodo.22235924 | RF-0002 related implementation evidence | Archived deterministic routing prototype; supports RF-0002 but does not by itself archive the RF-0002 disclosure text in this registry. |
| Resolutive Prior Art Registry v0.2.0 | 2026-09-05 | 10.5281/zenodo.22320536 | RM-0003 v0.2, RF-0002 v0.2, RT-0002 v0.3 plus registry snapshot | Second archival defensive-publication release; extends rather than replaces the historical v0.1.0 baseline. |

## Policy

- Prefer a DOI-backed archival deposit for stable releases intended as defensive technical publications.
- Record both version-specific DOI and concept DOI when the archive provides both.
- Never assign an archival DOI in this registry before the external record actually exists.
- Keep links between DOI, Git tag, release, disclosure IDs, and reference commits explicit.
- A DOI attached to a companion repository is evidence for that archived snapshot only; it must not be represented as automatically archiving later disclosures in this registry.
