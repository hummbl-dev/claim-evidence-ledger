# Public Research Citation Ledger Entry

Status: candidate example. This file illustrates a claim-evidence ledger entry and does not create canon.

## Claim

```text
Regular physical activity is associated with lower all-cause mortality risk in adults.
```

This example uses cautious association language. It does not claim that any single intervention guarantees a health outcome.

## Ledger Entry

```json
{
  "schemaVersion": "0.1",
  "packetStatus": "candidate",
  "ledgerManifest": {
    "id": "cel:example:physical-activity-mortality",
    "title": "Physical activity and mortality association example",
    "version": "0.1.0",
    "scope": "Single public research citation example for ledger shape."
  },
  "authority": {
    "id": "cel:authority:example-contributor",
    "name": "Example Contributor",
    "uri": "https://example.invalid/contributor"
  },
  "claimEvidenceContract": {
    "claim": "Regular physical activity is associated with lower all-cause mortality risk in adults.",
    "evidenceType": "public-research-citation",
    "sourceReference": {
      "type": "url",
      "uri": "https://pubmed.ncbi.nlm.nih.gov/25844730/",
      "contentHash": "not-captured-in-example"
    },
    "evidenceGrade": "public-indexed-research",
    "verificationStatus": "example-not-verified-live",
    "provenanceChain": [
      {
        "step": "source-selected",
        "actor": "example-contributor",
        "method": "public PubMed citation selected for schema demonstration"
      },
      {
        "step": "claim-softened",
        "actor": "example-contributor",
        "method": "used association language to avoid causal overclaim"
      }
    ],
    "receiptRef": {
      "receiptId": "receipt:example:claim-evidence-0001",
      "receiptUri": "examples/public-research-citation-ledger-entry.md"
    }
  },
  "receiptRequirements": {
    "inclusionProof": "none-for-example",
    "timestamp": true,
    "anchor": "example-file"
  }
}
```

## Receipt

- Added a public research citation example for claim-evidence ledger shape.
- Used cautious claim wording and marked live verification as not performed.
- Did not modify operator-authority surfaces.
- Did not introduce new HUMMBL/BaseN terminology.
