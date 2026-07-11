# Peptide Claim/Evidence Seed Dataset v0.1 — Edge-Case First

**Status: CANDIDATE DATASET — EDGE-CASE FIRST — NON-CLINICAL — NON-CANONICAL**

Issue: hummbl-dev/claim-evidence-ledger#9
Parent coordination: hummbl-dev/hummbl-dev#145
Schema/validator dependency: hummbl-dev/claim-evidence-ledger#8
Source registry dependency: hummbl-dev/hummbl-bibliography#77
Ontology dependency: hummbl-dev/knowledge-as-code#6

## Objective

Create the first validated peptide claim/evidence dataset using representative scientific and infrastructure records. The purpose is to force the schema through difficult identity, assay, context, contradiction, and evidence-stage cases — not to maximize record count.

A local ChatGPT package reportedly contained 29 seed claims. Those records are **not yet in this repository**. Reconstruct or import them only with source and validation receipts; do not claim the local count as repository state.

## Required representative subjects (12)

Include at least one bounded record set for each:

1. insulin or a specifically identified insulin chain/product context
2. oxytocin
3. secretin
4. a cyclic peptide
5. a RiPP
6. a nonribosomal peptide
7. an MHC-presented peptidoform
8. an antimicrobial or host-defense peptide
9. a venom peptide
10. a designed self-assembling peptide
11. a modified long-acting therapeutic peptide
12. a short-open-reading-frame micropeptide

These are ontology and evidence stress tests. They do not need equal depth.

## Required record families

For selected subjects, create linked records for:

- sequence identity
- peptidoform identity
- source record
- historical claim
- measurement/assay record
- contradiction or competing interpretation
- infrastructure claim (database, ontology, or registry)
- prediction vs observation boundary

## Required edge cases

The dataset must include:

- a "first" claim with explicit reference frame
- a record with conflicting labels across databases
- a record with missing assay context
- a record with a retracted or superseded source
- a prediction record clearly distinguished from observation
- a record with ambiguous modification or topology
- a record with a negative result explicitly labeled
- a record with a source license or access restriction

## Acceptance criteria

- [x] 12 representative subjects documented
- [x] 8 record families documented
- [x] 8 edge cases documented
- [ ] At least one bounded record set per subject exists in repository
- [ ] Every material claim has at least one source and exact locator where feasible
- [ ] More than half of load-bearing historical claims use primary or official sources
- [ ] Frame-dependent "first" claims include inclusion criteria and competing interpretations
- [ ] Regulatory sources record jurisdiction, status, issue date, and draft/final/superseded
- [ ] Source licenses/access restrictions are recorded
- [ ] No copyrighted source text copied beyond permitted quotation limits
- [ ] Valid machine-readable source/claim records parse successfully
- [ ] PR links to this issue and parent #145 and includes validation commands/results
- [ ] Independent reviewer checks provenance precision and claim wording

## Non-goals

- Declaring the dataset scientifically complete
- Copying full papers or proprietary database content
- Treating Nobel summaries as substitutes for all primary history
- Converting disputed history into a single unqualified narrative
- Recommending clinical or personal peptide use
- Introducing new HUMMBL/BaseN canon

## Cross-repo dependencies

- `hummbl-dev/hummbl-dev#145` — peptide science infrastructure (parent)
- `hummbl-dev/claim-evidence-ledger#8` — claim/evidence schema
- `hummbl-dev/hummbl-bibliography#77` — source registry
- `hummbl-dev/knowledge-as-code#6` — ontology/API

## Fact posture

This is a candidate dataset derived from issue #9. No claims about existing repository records. All subjects, families, and edge cases are candidate until validated.

## Receipt

- **Issue**: hummbl-dev/claim-evidence-ledger#9
- **Representative subjects**: 12
- **Record families**: 8
- **Edge cases**: 8
- **Cross-repo deps**: 4
- **Review status**: PENDING
