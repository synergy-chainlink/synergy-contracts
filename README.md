# SYNERGY

> The modern synthetic assets protocol which focus on raw materials.

The idea of the project is inspired by `Synthetix` and `FRAX` and `Overlay` protocols. Balance between over-collaterization part (which is represented by a users-shared debt pool) and algoritmic part (which is represented by a stake-insurance system) of the protocol gives the most stable and the closest peg over all existing synthetic assets protocols today.

## Contracts overview

The protocol consist of 4 main contracts

-   `Synergy` ─ The contract which performs rUSD (synthetic dollar) minting and burning for over-collateral in wETH (or analogue). It also tracks global debt.

-   `Synter` ─ The contract which rules synths. Synth minting, creating, burning, swapping process is provided by this contract.

-   `Loan` ─ The contract which allows users to borrow synths for over-collateral in rUSD. This lets users short synthetic assets. When an asset changes price, its shorts will decrease global debt while longs will increase it.

-   `Insurance` ─ The contract which implements the insurance logic. Users can stake RAW (Synergy's governance token) in order to secure their debt to the protocol from increasing. Insurance coverage depends on lockup time of staked RAW. Greater luckup time provides more available compensation.

And some other contracts

-   `Oracle` ─ The contract which provides asset prices.

-   `Raw` ─ The contract of the RAW token.

-   `Synt` ─ All synthetic assets base contract.

-   `Treasury` ─ Simple contract to collect protocol fees.
