# Peptide Claim/Evidence Ledger v0.1

**Status: CANDIDATE DOMAIN EXTENSION — REUSE EXISTING EVIDENCE GRAPH — NON-CANONICAL**

Issue: hummbl-dev/claim-evidence-ledger#8
Parent coordination: hummbl-dev/hummbl-dev#145
Source registry dependency: hummbl-dev/hummbl-bibliography#77

## Objective

Implement a peptide-domain claim/evidence ledger that extends the existing Cross-Repo Evidence Graph v0.1 rather than creating a competing evidence model.

The ledger must make peptide claims atomic, scope-bounded, source-linked, versioned, and capable of representing contradiction, failed replication, null evidence, and supersession.

## Governing invariant

> Every release-facing peptide claim resolves to an exact-enough subject identity, declared scope, evidence item, source/receipt posture, and bounded status—or remains candidate/unknown.

## Required claim schema

At minimum support:

```yaml
claim_id:
claim_text:
claim_type:
subject:
  id:
  type:
  label:
  version:
predicate:
object:
scope:
  scope_statement:
  species:
  tissue_or_cell:
  matrix:
  assay:
  conditions:
  dose_or_concentration:
  timepoint:
  comparator:
  uncertainty:
evidence:
  - evidence_id:
    evidence_type:
    source_id:
    source_type:
    url_or_locator:
    retrieval_date:
    confidence:
    stage:
    notes:
status:
  state:
  superseded_by:
  contradicted_by:
  replicated_by:
  failed_replication_by:
  corrected_by:
provenance:
  created_by:
  created_date:
  last_modified:
  review_status:
  review_by:
  review_date:
tags:
```

## Required evidence stages

```text
IN_VITRO
NONHUMAN_IN_VIVO
HUMAN_OBSERVATIONAL
CONTROLLED_CLINICAL
REGULATORY
META_ANALYSIS
FAILED_REPLICATION
NULL_RESULT
CONTRADICTED
SUPERSEDED
```

Evidence stages must not collapse into one stage.

## Required claim types

```text
OBSERVATION
MEASUREMENT
PREDICTION
INFERENCE
HYPOTHESIS
REGULATORY_STATEMENT
HISTORICAL_FACT
DEFINITIONAL
COMPARATIVE
```

## Required status states

```text
CANDIDATE
SUPPORTED
CONTRADICTED
SUPERSEDED
FAILED_REPLICATION
NULL
RETRACTED
UNKNOWN
```

## Required fixtures

### Valid fixtures

- valid single-source observation claim with full scope
- valid multi-source supported claim
- valid claim with contradiction and supersession chain
- valid regulatory claim with jurisdiction and effective date
- valid null result claim
- valid failed replication claim

### Invalid fixtures

- invalid claim with context collapse (in vitro -> human)
- invalid claim missing subject identity
- invalid claim with source prestige as confidence
- invalid claim missing scope statement
- invalid claim with prediction presented as observation
- invalid claim with no evidence linkage

## Acceptance criteria

- [x] Claim schema documented
- [x] 10 evidence stages defined
- [x] 9 claim types defined
- [x] 8 status states defined
- [x] 12 fixtures defined (6 valid, 6 invalid)
- [ ] JSON schema implemented
- [ ] Validator with deterministic checks
- [ ] Fixtures pass/fail as expected
- [ ] Cross-repo evidence graph integration
- [ ] Independent review completed

## Non-goals

- Creating a competing evidence model
- Defining peptide identity (knowledge-as-code owns that)
- Defining peptide sources (hummbl-bibliography owns that)
- Making medical recommendations
- Treating source prestige as confidence
- Collapsing evidence stages

## Cross-repo dependencies

- `hummbl-dev/hummbl-dev#145` — peptide science infrastructure (parent)
- `hummbl-dev/hummbl-bibliography#77` — peptide bibliography
- `hummbl-dev/knowledge-as-code#6` — peptide identity ontology
- `hummbl-dev/hummbl-dev#104` — Cross-Repo Evidence Graph v0.1
- `hummbl-dev/hummbl-dev#105` — evidence graph extension

## Fact posture

This is a coordination spec derived from issue #8. No claims about existing implementation. All schema fields and fixtures are candidate until validated.

## Receipt

- **Issue**: hummbl-dev/claim-evidence-ledger#8
- **Schema fields**: 20+ (claim, subject, scope, evidence, status, provenance)
- **Evidence stages**: 10
- **Claim types**: 9
- **Status states**: 8
- **Fixtures**: 12 (6 valid, 6 invalid)
- **Cross-repo deps**: 5
- **Review status**: PENDING
