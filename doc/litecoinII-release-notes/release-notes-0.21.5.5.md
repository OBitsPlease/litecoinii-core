LitecoinII 0.21.5.5 Release Notes
====================

LitecoinII has been updated to include the latest fixes and improvements from Litecoin Core v0.21.5.5.

This update includes important MWEB consensus hardening, improved node reliability, wallet and mining fixes, and additional validation enhancements for MimbleWimble Extension Blocks (MWEB).

Notable improvements include:

* Enhanced MWEB validation and state-handling protections
* Improved handling of invalid or mutated MWEB block data
* Hardened MWEB amount and fee calculations against overflow edge cases
* Improved chainstate replay and crash recovery reliability
* MWEB wallet and pegout accounting fixes
* Mining and `getblocktemplate` improvements for MWEB transactions
* Increased maximum P2P message size from 4MB to 32MB to better support valid MWEB blocks and messages
* Additional bug fixes, build improvements, and expanded testing coverage

To ensure smooth network activation of the new MWEB validation rules, LitecoinII introduces a future enforcement height at block 55,000. This gives miners, pools, exchanges, and node operators time to upgrade before stricter validation rules become active.

Upgrading is strongly recommended for all users, especially:

* miners
* mining pools
* exchanges
* public node operators
* users utilizing MWEB functionality

Older wallet versions may continue operating temporarily before enforcement activates, but upgraded versions are recommended to ensure full compatibility with future consensus rules and MWEB validation improvements.

More details at Litecoin's [release-notes-0.21.5.5](https://github.com/litecoin-project/litecoin/blob/master/doc/litecoin-release-notes/release-notes-0.21.5.5.md)