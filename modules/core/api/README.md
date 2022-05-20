# API

This module allows you to fetch data from the stacks-blockchain-api. It exports a set of fetchers that map to all available endpoints in the API.

```typescript
import * as client from 'micro-stacks/api';
```

### Endpoints

* [Accounts](accounts.md)
* [Blocks](blocks.md)
* [BNS](bns.md)
* [Burnchain](burnchain.md)
* [Faucets](faucets.md)
* [Fee Rate](fee-rate.md)
* [Fees](fees.md)
* [Info](info.md)
* [Microblocks](microblocks.md)
* [Search](search.md)
* [Smart Contracts](smart-contracts.md)
* [Tokens](tokens.md)
* [Transactions](transactions.md)

### The Stacks 2.0 Blockchain API

The Stacks 2.0 Blockchain API is an API service developed and ran by [Hiro Systems PBC](https://hiro.so). This API provides endpoints for developers to fetch data from the Stacks blockchain and interface with Clarity smart contracts.&#x20;

`micro-stacks` aims to provide a complete and easy to use Stacks API client implementation, thereby reducing the amount of boilerplate needed to launch a Stacks app.

The Stacks API consists of two separate but related services:

* The **Stacks Blockchain API** that provides _extended_ endpoints for additional capabilities (these routes can be identified by the `/extended/` path.
* The **Stacks Node** that exposes a JSON RPC API (these routes can be identified by the `/v2/` path.

In the client code and API examples within this document, we reference the Stacks API implementations freely hosted by [Hiro](https://hiro.so/):

`mainnet: https://stacks-node-api.mainnet.stacks.co/`

`testnet: https://stacks-node-api.testnet.stacks.co/`

The hosted Stacks API offers a quick onboarding environment for developers to get started. To provide end users with a more decentralized architecture, consider [hosting your own Stacks API](https://docs.hiro.so/get-started/running-api-node).

#### More resources

1. [https://docs.hiro.so/get-started/stacks-blockchain-api](https://docs.hiro.so/get-started/stacks-blockchain-api)
