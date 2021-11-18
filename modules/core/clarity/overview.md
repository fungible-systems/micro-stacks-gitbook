# Overview

## What is Clarity?

Clarity is a smart contract language for Bitcoin that runs on Stacks. `micro-stacks` provides an intuitive interface for interacting with published Clarity contracts via the [Stacks API](../../../the-stacks-2.0-blockchain-api.md).&#x20;

Clarity has a number of important advantages that make it easy for developers to create expressive contracts that execute predictably and safely. Here are a few of the highlights:

* Code is published directly to the blockchain without being compiled, i.e., it's an _interpreted_ language
* _Overflow / underflow guards _ensure a transaction will automatically abort rather than continue to execute chaotically
* _Strongly typed_ with no type mixing means variables can only store values of the correct type
* No smart contract anti-features, such as Turing Completeness mean it's _decidable_.
* Custom _fungible and non-fungible tokens (NFTs)_ are built in the language itself
* Contracts can natively read the state of the Bitcoin settlement layer and use _Bitcoin transactions_ as a trigger&#x20;
* Transactions can be secured by [_Post Conditions_](post-conditions.md) which enforce a pre-defined end state for any token transfers that end users can view prior to execution

You can learn more about Clarity in the resources linked below.

#### Further reading:

1. [https://clarity-lang.org/](https://clarity-lang.org)
2. [https://book.clarity-lang.org/](https://book.clarity-lang.org)
3. Start writing smart contracts in the REPL [https://hirosystems.github.io/clarity-repl/](https://hirosystems.github.io/clarity-repl/)

## How do JavaScript apps use Clarity?

