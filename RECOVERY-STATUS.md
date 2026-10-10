# LitecoinII Recovery Status

Updated: 2026-10-10

## Active maintainer

LitecoinII (LC2) has an active recovery and maintenance effort led through the
GitHub account [@OBitsPlease](https://github.com/OBitsPlease). OBitsPlease is
the current project maintainer and the only maintainer authorized by this
repository.

The previous source repository became unavailable. This repository preserves
recovered LC2 Core v0.21.6.0 source while its provenance, tests, live-chain
compatibility, and release process are independently re-established.

## Former developer status

The former LitecoinII developer is no longer involved in LC2 development,
maintenance, governance, releases, fundraising, or decisions made through this
repository. The former developer does not speak for this recovery effort and
is not authorized to request funds, publish releases, issue operator guidance,
or represent the project on its behalf.

Previous project accounts, contact addresses, websites, signing identities,
and announcements must not be treated as current or authorized unless
OBitsPlease explicitly verifies them through this repository. The current
maintainer does not plan to restore the former developer to a project role.

## Guidance for pools and exchanges

- LC2 development and maintenance are active.
- Treat OBitsPlease as the current point of contact for this recovery effort.
- Do not rely on instructions or funding requests attributed to the former
  developer.
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
