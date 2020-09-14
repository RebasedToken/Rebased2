# Rebased v2

Rebased is a trustless elastic supply currency that adjusts its supply without reliance on external price feeds. It is a fork of the [uFragments protocol](https://github.com/ampleforth/uFragments). Version 2 adds protection features such as atomic notfication of liqudity pools of balance changes.

The smart contracts in this repository are already flattened and deployment-ready. The system consists of the following components:

- RebasedV2: Version 2 of the Rebased ERC20 elastic supply token. 
- RebasedController: Contains configuration options, the rebase function and configurable list of post-rebase transaction hooks for syncing liquidity pools and updating the Oracle.
- RebasedOracle: A price feed that calculates the average token price since the previous rebase. Uses Uniswap V2 oracles as the input and is meant to be refreshed after every rebase by the controller.
