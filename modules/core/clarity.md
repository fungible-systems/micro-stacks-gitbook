# Clarity

### What is Clarity?

Clarity is a smart contract language for Bitcoin that runs on the Stacks blockchain. `micro-stacks` provides an intuitive interface for interacting with Clarity via JavaScript.

Clarity has a number of advantages that make it easy for developers to create expressive contracts that execute predictably and safely. Here are a few of the highlights:

* Clarity code is published directly to the blockchain without being compiled, i.e., it's an _interpreted_ language
* _Overflow / underflow guards _ensure a transaction will automatically abort rather than continue to execute chaotically
* _Strongly typed_ with no type mixing means variables can only store values of the correct type
* No smart contract anti-features, such as Turing Completeness, which means Clarity is _decidable_
* Custom _fungible _and_ non-fungible tokens (NFTs)_ are built-in primitives in the language
* Contracts can natively read the state of the Bitcoin settlement layer and use _Bitcoin transactions_ as a trigger&#x20;
* Transactions can be secured by [_Post Conditions_](clarity/post-conditions.md) which enforce a pre-defined end state for any token transfers that end users can view prior to execution

You can learn more about Clarity in the resources linked below.

#### Further reading:

1. [https://clarity-lang.org/](https://clarity-lang.org)
2. [https://book.clarity-lang.org/](https://book.clarity-lang.org)
3. Start writing smart contracts in the REPL [https://hirosystems.github.io/clarity-repl/](https://hirosystems.github.io/clarity-repl/)

### micro-stacks/clarity

The Clarity module in micro-stacks exports everything you need to start interacting with clarity code in your app. Check out the pages below to see how to use this module:

{% content-ref url="clarity/clarity-values.md" %}
[clarity-values.md](clarity/clarity-values.md)
{% endcontent-ref %}

{% content-ref url="clarity/serialization.md" %}
[serialization.md](clarity/serialization.md)
{% endcontent-ref %}

{% content-ref url="clarity/post-conditions.md" %}
[post-conditions.md](clarity/post-conditions.md)
{% endcontent-ref %}
