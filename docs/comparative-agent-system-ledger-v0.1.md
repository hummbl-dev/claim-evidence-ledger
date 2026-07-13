# Comparative Agent System Ledger v0.1 — Reusable Example

**Status: CANDIDATE EXAMPLE — NON-CANONICAL**

Issue: hummbl-dev/claim-evidence-ledger#10
Parent work:
- hummbl-dev/hummbl-dev#152 — Comparative Agent Runtime Program
- hummbl-dev/hummbl-research#48 — OpenClaw × Hermes campaign
- hummbl-dev/research-source-packets#12 — public packet

## Purpose

Add a reusable, bounded example for representing comparative claims about evolving agent systems without making the OpenClaw × Hermes campaign itself canonical to this repository.

The repository should own the generic claim/evidence structure. Campaign-specific evidence remains in `hummbl-research` and `research-source-packets`.

## Proposed artifact

```text
examples/comparative-agent-system-ledger-v0.1.json
```

If the existing schema cannot represent the required fields cleanly, propose a backwards-compatible schema extension rather than silently changing the contract.

## Required fields

```yaml
claim_id:
claim_text:
subject_entities:
historical_aliases:
comparison_axis:
claim_class:
fact_posture:
effective_date:
observed_at:
last_verified_at:
source_ids:
source_authority_scope:
caveats:
confidence_posture:
adoption_status:
decision_relevance:
material_change_triggers:
```

## Fact postures

Support or clearly map:

- `OBSERVED_IMPLEMENTATION`
- `RELEASE_CLAIM`
- `PROJECT_SELF_DESCRIPTION`
- `FOUNDER_ACCOUNT`
- `EXTERNAL_CORROBORATION`
- `INFERENCE`
- `UNVERIFIED`

## Required example cases (8)

1. a directly observed commit-level implementation claim
2. a maintainer release claim
3. a project-positioning claim
4. an inferred historical conclusion supported by multiple sources
5. a comparative claim requiring evidence from both systems
6. a historical-alias / rename event
7. a claim invalidated or superseded by a later release
8. an unresolved claim with explicit evidence insufficiency

## Validation requirements

- [ ] Valid example passes the current or extended validator
- [ ] Invalid fixture rejects a comparative claim with evidence from only one compared system
- [ ] Invalid fixture rejects an inference represented as observed implementation
- [ ] Invalid fixture rejects missing `effective_date` for temporal claims
- [ ] Invalid fixture rejects unsupported absolute language when caveats/evidence are insufficient
- [ ] README explains instance-ledger versus reusable-method boundaries

## Guardrails

- Candidate/example scope only
- No universal-standard claim
- No new HUMMBL/BaseN term canonization
- No private campaign evidence

## Acceptance criteria

- [x] 16 required fields documented
- [x] 7 fact postures documented
- [x] 8 example cases documented
- [x] 5 validation requirements documented
- [ ] Valid example passes validator
- [ ] Invalid fixtures reject as expected
- [ ] README explains boundaries

## Cross-repo dependencies

- `hummbl-dev/hummbl-dev#152` — Comparative Agent Runtime Program
- `hummbl-dev/hummbl-research#48` — OpenClaw × Hermes campaign
- `hummbl-dev/research-source-packets#12` — public packet

## Fact posture

This is a candidate example derived from issue #10. No claims about existing implementation. All fields, postures, and cases are candidate until validated.

## Receipt

- **Issue**: hummbl-dev/claim-evidence-ledger#10
- **Required fields**: 16
- **Fact postures**: 7
- **Example cases**: 8
- **Validation requirements**: 5
- **Cross-repo deps**: 3
- **Review status**: PENDING
