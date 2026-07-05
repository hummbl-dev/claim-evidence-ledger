# Claim-Evidence Ledger v0.1 Packet Receipt

This is a candidate, non-normative receipt template for a v0.1 claim-evidence packet.
In v0.1 the receipt is a structural placeholder describing what a future
cryptographically verifiable receipt must contain. It is not itself a cryptographic
proof.

## Non-canon note

This template describes the shape of a receipt, not a verified proof. Verification of
receipts is out of scope for v0.1.

## Fields

A v0.1 packet receipt should record:

- `receiptId` — identifier matching `claimEvidenceContract.receiptRef.receiptId`.
- `packetHash` — content hash of the packet the receipt covers.
- `ledgerId` — identifier matching `ledgerManifest.id`.
- `inclusionProof` — proof type (e.g. `merkle`, `chainpoint`, `opentimestamps`).
- `proof` — the proof payload (Merkle path, timestamp anchor, etc.).
- `timestamp` — time the receipt was issued.
- `anchor` — anchor type for the timestamp (e.g. `internal`, `bitcoin`, `ethereum`).
- `issuer` — identifier of the receipt issuer.

## Example shape

```json
{
  "receiptId": "receipt:example:0001",
  "packetHash": "sha256:...",
  "ledgerId": "cel:example:provenance-demo",
  "inclusionProof": "merkle",
  "proof": {
    "merklePath": [],
    "merkleRoot": "sha256:..."
  },
  "timestamp": "2025-01-15T12:00:00Z",
  "anchor": "internal",
  "issuer": "cel:authority:example-issuer"
}
```

## Review expectations

Reviewers should check that:

- The receipt fields align with the packet's `receiptRequirements`.
- The `receiptId` matches the packet's `receiptRef.receiptId`.
- The `ledgerId` matches the packet's `ledgerManifest.id`.

Reviewers are not expected to verify cryptographic proof payloads in v0.1.
