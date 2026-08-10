# The Second Nature — Verification Manifest

This manifest accompanies the canonical publication of *The Second Nature*, V1.0.
It exists outside the essay by construction: a document cannot contain its own hash.

## Canonical artifact (anchored)
- File: `the-second-nature-v1.0.md` (UTF-8 Markdown — the canonical text)
- SHA-256: `2563c65ab5c416de432aacb50c8086b94bce5da78c49876eacbf541344905b8e`

## Reading rendition
- File: `The-Second-Nature-V1.0.pdf` (typeset rendition of the canonical text)
- SHA-256: `e67cab3ba7a983ee1941a90ca546f9f6c7def650bc271ffcb86e2450eb083590`

## Bitcoin anchor
- OP_RETURN payload: `ANCHOR-V2` + SHA-256 of the canonical artifact
- Transaction ID: `12a1d28720ed1b5b904bdee8fe4805168e03c993834b743499737053fb4b0ef0`
- Block height: `961866` (mined by Foundry USA, 2026-08-10 12:43 CEST)
- The anchor spends the change of the first essay's dialogue anchor (`ANCHOR-D1`,
  block 960884): the artifacts of this authorship form one unbroken transaction chain,
  from the funding at block 960849 through essay one (`ANCHOR-V1`, block 960856), the
  authorship commitment (`ANCHOR-ID1`, block 960869), and the dialogue manifest, to this
  essay — each anchor paid from the change of its predecessor.
- OpenTimestamps proofs: `the-second-nature-v1.0.md.ots` and `The-Second-Nature-V1.0.pdf.ots` (in this repository); calendar attestations are upgraded to Bitcoin attestations as they confirm.
  
## The first essay
- *The Last Scarce Good* — canonical home and verification manifest:
  https://nullius2140.github.io/the-last-scarce-good/

## How to verify
1. Obtain the canonical file from this repository.
2. Compute: `sha256sum the-second-nature-v1.0.md` (macOS: `shasum -a 256 …`)
3. Compare against the OP_RETURN payload of the transaction above.

## Note on this manifest
This file is the living outer layer of the verification architecture. The anchored
artifact is immutable; this manifest is updated as the anchor confirms (block height)
and as secondary attestations (OpenTimestamps) are published. The chain, not this
file, is the authority: every claim here is checkable against it.
