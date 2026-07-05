# Prior Art and Adjacent Ecosystem

This document collects public prior art and adjacent ecosystem references relevant to
claim-evidence ledgers. It is non-exhaustive and explicitly **non-canon**: listing an
entry here acknowledges its existence and relevance, not derivation, endorsement, or
ownership.

## Non-canon note

This repository does not claim to have invented claim-evidence ledgers, append-only
logs, cryptographic receipts, or any related concept. The vocabulary below is
descriptive. Where this repository's candidate patterns overlap with existing public
work, that public work is the authoritative reference.

## Public prior art

### Carbonchain

- **What it does:** Public work on supply-chain and commodity emissions accounting,
  treating claims about carbon and provenance as auditable records.
- **Relevance:** Demonstrates treating environmental and supply-chain claims as
  evidence-backed, reviewable ledger entries rather than free-text assertions.
- **Docs:** https://www.carbonchain.com/

### Krineia

- **What it does:** Public work on verifiable data and audit structures.
- **Relevance:** Adjacent approach to structuring claims and evidence for review and
  verification.
- **Docs:** https://github.com/krineia

### Sigstore / Rekor

- **What it does:** Sigstore provides software signing for open source; Rekor is its
  append-only, tamper-evident transparency log of signing events.
- **Relevance:** A production-grade append-only transparency log with receipts and
  inclusion proofs. A direct reference model for cryptographic receipts and
  tamper-evidence in a claim-evidence ledger.
- **Docs:** https://docs.sigstore.dev/ / https://github.com/sigstore/rekor

### Certificate Transparency Logs

- **What it does:** Public append-only logs of issued TLS certificates, with Merkle
  inclusion proofs and monitoring/auditing infrastructure.
- **Relevance:** The canonical public example of an append-only, tamper-evident
  transparency log with third-party auditability.
- **Docs:** https://certificate.transparency.dev/

### Amazon QLDB

- **What it does:** A managed ledger database providing a transparent, immutable, and
  cryptographically verifiable transaction log.
- **Relevance:** Demonstrates cryptographic verification of an append-only ledger with
  a journal and digest-based proof.
- **Docs:** https://aws.amazon.com/qldb/

### Hyperledger Fabric

- **What it does:** A permissioned distributed ledger platform with pluggable
  endorsement, ordering, and ledger semantics.
- **Relevance:** Demonstrates ledger data models, endorsement policies, and provenance
  tracking for auditable records.
- **Docs:** https://hyperledger-fabric.readthedocs.io/

### Chainpoint

- **What it does:** A standard for anchoring data to a blockchain and returning a
  cryptographic receipt with Merkle inclusion proofs.
- **Relevance:** A direct reference model for receipt structure and proof formats for
  ledger entries.
- **Docs:** https://chainpoint.org/

## Adjacent ecosystem

### IPFS

- **What it does:** A peer-to-peer protocol for content-addressed storage and
  retrieval.
- **Relevance:** Provides a content-addressable substrate for storing evidence and
  source references behind a claim.
- **Docs:** https://docs.ipfs.tech/

### Filecoin

- **What it does:** A decentralized storage network providing verifiable storage over
  time via proofs-of-spacetime.
- **Relevance:** Demonstrates verifiable, time-anchored storage of evidence.
- **Docs:** https://docs.filecoin.io/

### Arweave

- **What it does:** A permanent, append-only storage network with economic
  endowment-based permanence.
- **Relevance:** Demonstrates append-only, permanent storage as an evidence substrate.
- **Docs:** https://docs.arweave.org/

### OpenTimestamps

- **What it does:** A system for proving a piece of data existed at a given time by
  anchoring a hash to the Bitcoin blockchain.
- **Relevance:** A minimal, production reference for timestamp receipts and inclusion
  proofs.
- **Docs:** https://opentimestamps.org/

### Merkle trees

- **What it does:** A hash tree data structure enabling efficient, tamper-evident
  inclusion proofs over append-only data.
- **Relevance:** The core cryptographic primitive behind transparency logs and
  receipts used in this field.
- **Docs:** https://en.wikipedia.org/wiki/Merkle_tree

### Append-only logs

- **What it does:** A data structure that only allows appending, enabling
  tamper-evidence and auditability.
- **Relevance:** The foundational structure for any claim-evidence ledger that wants
  to preserve provenance over time.
- **Docs:** https://en.wikipedia.org/wiki/Append-only

### Content-addressable storage

- **What it does:** Storage keyed by the cryptographic hash of its contents, so
  retrieval also verifies integrity.
- **Relevance:** The natural storage model for evidence referenced by a claim-evidence
  packet.
- **Docs:** https://en.wikipedia.org/wiki/Content-addressable_storage

## Vocabulary

The following terms are used descriptively in this repository. They are not
proprietary and are not canonized here.

- **Claim** — a statement asserted as true, pending evidence.
- **Evidence** — material referenced in support of a claim.
- **Ledger** — an append-only, tamper-evident record of entries.
- **Provenance** — the origin and chain of custody for a piece of data.
- **Attestation** — a signed statement vouching for a fact or relationship.
- **Receipt** — a cryptographic proof that an entry was included in a ledger.
- **Append-only** — a constraint that data may be added but not modified or deleted.
- **Tamper-evident** — a property where unauthorized modification is detectable.

## Key concepts

- **Claim-evidence pairs** — the atomic unit: a claim plus the evidence offered for it.
- **Provenance chains** — a sequence of records showing where evidence came from and
  how it was handled.
- **Append-only ledgers** — ledgers that only grow, preserving history and enabling
  audit.
- **Cryptographic receipts** — machine-verifiable proofs of inclusion in a ledger.
- **Audit trails** — reviewable records of who did what, when, and against what
  evidence.
- **Evidence grading** — a scheme for expressing confidence or quality of evidence
  behind a claim (candidate in v0.1, not normative).
