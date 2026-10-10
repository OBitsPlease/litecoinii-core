# Recovered Source Provenance

## Status

This repository began as a recovery candidate after the original
`litecoinII-project/litecoinII` repository became unavailable.

The initial commit contains the recovered source tree without source-code
changes. The original Git history was not present in the recovered archive and
has not been reconstructed.

This source must not be described as canonical, and binaries built from it must
not be presented as canonical releases, until the verification gates below are
complete.

## Recovered artifact

- Archive: `litecoinII-0.21.6.0.sourcecode.tar.gz`
- SHA-256:
  `C9442197D120F06DFDF1A29CAB81AFF507157809055F26B4300ED8C3AF3027C6`
- Recovered version: LitecoinII Core v0.21.6.0
- Initial recovered-source commit:
  `6ebe9f9b4454c13841aeefc4db506fbd39833932`
- License: MIT; existing Bitcoin Core, Litecoin Core, and LitecoinII
  attribution is retained in `COPYING`.

The original archive is preserved separately and must remain unchanged.

## Verification gates

Before publishing new binaries as canonical:

1. Build the source successfully in a clean environment.
2. Run unit and regtest coverage.
3. Verify the expected genesis block and consensus parameters.
4. Synchronize a rebuilt node against a copied data directory.
5. Confirm the rebuilt node follows the existing network to the same best block
   hash as an independently trusted node.
6. Compare independently built artifacts.
7. Document reproducibility or any accepted sources of non-reproducibility.
8. Publish signed checksums and release notes through an approved signing
   identity.

## Change policy during recovery

- Keep consensus recovery separate from miner fee and operations changes.
- Do not change genesis, proof-of-work, difficulty adjustment, subsidy,
  activation heights, network magic, ports, or address prefixes without a
  separately reviewed and explicitly approved network proposal.
- Record each validation result with the exact source commit, environment, and
  commands used.
- Do not commit wallets, private keys, seed phrases, RPC credentials, node
  cookies, logs containing secrets, or live blockchain data.

