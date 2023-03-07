# `recovery`

Recover tokens that are stuck on unsupported Match accounts.

## Abstract

This document specifies the  `x/recovery` module of the Match Hub.

The `x/recovery` module enables users on Match to recover locked funds
that were transferred to accounts whose keys are not supported on Match.
This happened in particular after the initial Match launch (`v1.1.2`),
where users transferred tokens to a `secp256k1` Match address via IBC
in order to [claim their airdrop](./../modules/claims/concepts).
To be EVM compatible,
[keys on Match](./../concepts/accounts#match-accounts) are generated
using the `eth_secp256k1` key type which results in a different address derivation
than e.g. the `secp256k1` key type used by other Cosmos chains.

At the time of Match’ relaunch,
the value of locked tokens on unsupported accounts sits at $36,291.28 worth of OSMO and $268.86 worth of ATOM tokens
according to the [Mintscan](https://www.mintscan.io/match/assets) block explorer.
With the `x/recovery` module, users can recover these tokens back to their own addresses
in the originating chains by performing IBC transfers from authorized IBC channels
(i.e. Osmosis for OSMO, Cosmos Hub for ATOM).

## Contents

1. **[Concepts](01_concepts.md)**
2. **[Hooks](02_hooks.md)**
3. **[Events](03_events.md)**
4. **[Parameters](04_parameters.md)**
5. **[Clients](05_clients.md)**