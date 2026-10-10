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
  `1c874c750ca024b4143065c87b5186206832fa92`
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

## Verification record

### 2026-10-10: Initial Linux build and offline checks

Source commit: `357cdae`

Environment:

- WSL 2
- Ubuntu 22.04.5 LTS
- GCC/G++ 11.4.0
- Wallet and GUI disabled because the environment does not provide the portable
  Berkeley DB 4.8 dependency

Results:

- `./autogen.sh`: passed
- `./configure --without-gui --disable-wallet --disable-bench --disable-fuzz-binary`:
  passed
- `make -j$(nproc)`: passed
- Consensus-focused Boost suites `pow_tests`, `validation_tests`, and
  `scrypt_tests`: 17 test cases passed with no errors
- `feature_config_args.py`: passed against the rebuilt daemon in regtest mode
- Offline mainnet startup with networking disabled: passed; `getblockhash 0`
  returned
  `fefb8200c7da35576d1d54ede22de1e69f5d8a5ee598b7535548d9632b367e3b`,
  matching `chainparams.cpp`

Known failure:

- Full `make check` stops in
  `blockfilter_index_tests/blockfilter_index_initial_sync` because
  `CreateNewBlock` creates a transaction rejected as `bad-txns-vin-empty`.
  This must be investigated before the unit-test verification gate can pass.

These results do not cover wallet builds, the complete unit suite, live-chain
compatibility, or reproducibility. They do not authorize publication of new
binaries as canonical releases.

## Change policy during recovery

- Keep consensus recovery separate from miner fee and operations changes.
- Do not change genesis, proof-of-work, difficulty adjustment, subsidy,
  activation heights, network magic, ports, or address prefixes without a
  separately reviewed and explicitly approved network proposal.
- Record each validation result with the exact source commit, environment, and
  commands used.
- Do not commit wallets, private keys, seed phrases, RPC credentials, node
  cookies, logs containing secrets, or live blockchain data.
