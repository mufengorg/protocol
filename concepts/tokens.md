---
sidebar_position: 11
---

# Tokens

## The MATCH Token

The denomination used for staking, governance and gas consumption on the EVM is the MATCH. The MATCH provides the utility of: securing the Proof-of-Stake chain, token used for governance proposals, distribution of fees to validator and users, and as a mean of gas for running smart contracts on the EVM.

Match uses [Atto](https://en.wikipedia.org/wiki/Atto-) MATCH as the base denomination to maintain parity with Ethereum.
There are three types of assets:

- The native Match token
- IBC Coins (via the IBC)
- Ethereum-typed tokens, e.g. ERC-20

`1 match = 10<sup>18</sup> amatch`

This matches Ethereum denomination of:

`1 ETH = 10<sup>18</sup> wei`

## Cosmos Coins

Accounts can own Cosmos coins in their balance, which are used for operations with other Cosmos and transactions. Examples
of these are using the coins for staking, IBC transfers, governance deposits and EVM.

## EVM Tokens

Match is compatible with ERC20 tokens and other non-fungible token standards (EIP721, EIP1155)
that are natively supported by the EVM.

## Match Assets Page

Check out how we represent ERC-20 tokens and Cosmos IBC Coins through our [Single Token Representation](https://app.match.org/assets)
feature on the Match Dashboard. Match enabled this feature to help with the user experiences by obfuscating the assets
types away from the users and allow them to focus on the interaction. The protocol simplifies the process by handling the
conversion and users are given the simplification of denomination and the amount of assets they hold.

![match-dashboard-assets])(/img/dashboard-assets.png)

For more information on how we handle token registration, head over [here](./../../develop/mainnet#token-registration).
