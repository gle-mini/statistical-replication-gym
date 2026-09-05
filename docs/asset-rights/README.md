# Asset-rights register

[register.csv](register.csv) records third-party assets considered for SRG.
It is initially empty because no studies or external assets have been admitted.
An empty register is not approval of any future asset.

Create one row per paper, dataset/version, author-code release, figure/table,
or derived artifact before including it in a task package or public export.
Use separate rows when components have different terms. Record candidates even
when rights are unresolved or redistribution is prohibited.

## Fields

| Field | Required content |
| --- | --- |
| `asset_id` | Stable unique identifier referenced by the task manifest. |
| `study_id` | Candidate/task identifier, or `not-assigned` during triage. |
| `asset_type` | `paper`, `data`, `code`, `figure`, `table`, or `derived`. |
| `source_url` | Canonical source or persistent identifier. |
| `version` | Release, revision, or retrieval date identifying the asset. |
| `sha256` | Content checksum when lawfully acquired; otherwise `not-acquired`. |
| `rights_holder` | Named rights holder, or `unknown` with an open question. |
| `license_or_terms` | SPDX identifier where applicable, or precise terms/permission reference; `unknown` if unresolved. |
| `evidence_url` | Source license/terms URL or durable permission evidence reference; never expose private correspondence. |
| `access_conditions` | Public, registration, agreement, or other requirements, including permitted execution/use. |
| `redistribution` | `permitted`, `conditional`, `prohibited`, or `unknown`. |
| `obligations` | Attribution, notices, modification marking, share-alike, use limits, or other applicable conditions; use `none-documented` only with evidence. |
| `acquisition_instructions` | Instructions or script path for permitted access when the asset is not bundled. |
| `review_status` | `pending`, `approved`, or `blocked`; approval concerns the documented intended use only. |
| `reviewer` | Reviewer identity, or `pending`. |
| `reviewed_on` | Review date (`YYYY-MM-DD`), or `pending`. |
| `notes` | Intended use, distribution destination, parent asset IDs for derivatives, and unresolved questions. |

Use valid CSV quoting for commas and line breaks. Do not leave unknown rights
implicit: use the explicit unresolved values and explain the missing evidence.

## Review and distribution gate

The contributor supplies evidence and the maintainer or designated reviewer
checks it before approving the intended use. This rights review is separate
from the independent scientific review of the statistical reference.

Approve public inclusion only when redistribution is `permitted` or
`conditional`, the applicable obligations have been met, and no unresolved
access, privacy, consent, or other restriction blocks the intended publication.
Record the reviewer and date. Unknown or conflicting terms block redistribution
until resolved; mere public availability never establishes permission.

An asset marked `prohibited` for redistribution may still support a task through
lawful user acquisition, provided the intended execution/use is permitted and
the package does not include the restricted asset. Record that distinction in
the review and acquisition instructions. If access/use is also unavailable or
unclear, mark the intended use blocked.

Recheck the entry when sources, versions, terms, or intended uses change, and
before a release/export. Keep previous review evidence in version control.
Do not apply the project's original-code or documentation license to external
papers, data, code, or derived content without authority to do so.
