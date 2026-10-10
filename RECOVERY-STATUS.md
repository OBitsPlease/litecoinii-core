# LitecoinII Recovery Status

Updated: 2026-10-10

## Active maintainer

LitecoinII (LC2) has an active recovery and maintenance effort led through the
GitHub account [@OBitsPlease](https://github.com/OBitsPlease).

The previous source repository became unavailable. This repository preserves
recovered LC2 Core v0.21.6.0 source while its provenance, tests, live-chain
compatibility, and release process are independently re-established.

## Guidance for pools and exchanges

- LC2 development and maintenance are active.
- No consensus change, chain restart, swap, or address-format change is
  announced by this recovery repository.
- Existing operators should continue using their currently validated LC2
  deployment while recovery verification is in progress.
- Do not treat binaries built from this repository as canonical releases yet.
- Do not download replacement binaries from unverified third parties.
- Monitor this repository for verified source status, signed checksums, release
  policy, and future operator notices.

Pools and exchanges are invited to open a GitHub issue for non-sensitive
integration questions or join the community at
https://discord.gg/v4YGTDt65.

## Verification completed so far

- Original recovered source archive hash recorded.
- Recovered source imported without intentional consensus changes.
- Wallet-disabled Linux build completed successfully.
- Genesis, Scrypt/PoW, subsidy, and validation-focused tests passed.
- Rebuilt daemon started successfully in regtest.
- Offline mainnet genesis hash matched the recovered chain parameters.

See [RECOVERY-PROVENANCE.md](RECOVERY-PROVENANCE.md) for exact commands,
environment details, known failures, and remaining verification gates.

## Remaining gates

- Resolve the known full unit-suite failure.
- Complete a wallet-capable build with the required portable dependencies.
- Compare a rebuilt node against the existing live chain and a trusted tip.
- Establish reproducible builds, signing identity, and release approvals.
- Publish verified releases and checksums only after those gates pass.

## Scope warning

This repository establishes continuity of maintenance; it does not yet claim
that newly built binaries are canonical. No recovered wallets, credentials,
private keys, logs, or live blockchain data are stored here.
