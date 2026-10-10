LitecoinII Core v0.21.6.0 Release Notes
====================

LitecoinII Core v0.21.6.0 introduces a custom **Linear Weighted Moving Average difficulty adjustment algorithm (LWMA)**.

The new difficulty rules activate on the main network at block height **65273**.

```text
Last block using the previous difficulty rules: 65272
First block using LWMA:                         65273
```

LWMA recalculates mining difficulty after every block and responds more quickly to changes in network hashrate. This is intended to provide more consistent block times and reduce long periods of unusually fast or slow blocks.

This release does not change the block reward, maximum supply, halving schedule, target block time, addresses, private keys, wallet files, or existing balances.

This is a **mandatory consensus upgrade**. Miners, pools, exchanges, explorers, Electrum servers, and other node operators must upgrade before block height **65273**.

A blockchain reindex is not normally required.
