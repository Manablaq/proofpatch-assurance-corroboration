# ProofPatch Assurance Corroboration Publisher

Canonical independent corroboration publisher for ProofPatch V3 assurance.

Authority identity:

`Manablaq/proofpatch-assurance-corroboration`

Approved raw prefix after repository creation:

`https://raw.githubusercontent.com/Manablaq/proofpatch-assurance-corroboration/`

## Role

This repository independently publishes release-specific corroborating
assurance evidence. It must not merely copy the primary publisher's verdict.
The raw facts must independently support the same validator-derived assurance
vector.

See `ASSURANCE_EVIDENCE_SCHEMA.md`.

## Publication rules

- Public repository.
- Evidence files are JSON.
- Every evidence URL used on-chain must include a 40-character lowercase commit
  SHA in the raw GitHub URL.
- Never reuse an `evidence_id`.
- Primary and corroboration evidence IDs must differ.
- `published_at` and `expires_at` are Unix seconds.
- Evidence must be fresh under the target's `max_evidence_age_seconds`.
- Do not rewrite or silently replace already-referenced evidence.
