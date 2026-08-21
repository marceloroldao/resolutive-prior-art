# Contributing

This repository is a publication registry, not a scratchpad. Contributions should improve a defined disclosure, supporting evidence, or registry metadata.

## Contribution workflow

1. Create or update a disclosure on a non-default branch.
2. Use an existing permanent ID or reserve a new ID in `registry/INDEX.md`.
3. Start from `templates/DISCLOSURE_TEMPLATE.md`.
4. Separate demonstrated behavior from hypotheses and future work.
5. Link exact implementation commits and reproducibility evidence when applicable.
6. Submit changes for review before merging to the default branch.
7. Freeze stable public sets through tagged releases; archival DOI publication is a separate deliberate step.

## Required discipline

Do not:

- rewrite historical published claims without versioning;
- present untested hypotheses as validated results;
- publish credentials, private keys, customer information, or production secrets;
- use marketing superlatives as substitutes for technical evidence;
- claim universal O(1), determinism, compression, accuracy, or other properties beyond the scope actually demonstrated.

## Preferred language

Normative specifications should use clear technical language. Terms such as MUST, SHOULD, and MAY may be used in protocol specifications when their normative meaning is defined in the document.
