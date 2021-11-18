---
description: Stacks Node, Stacks Blockchain API
---

# The Stacks 2.0 Blockchain API

The Stacks 2.0 Blockchain API (Stacks API) provides endpoints for developers to fetch data from the Stacks blockchain and interface with [Clarity smart contracts](modules/core/clarity/). `micro-stacks` aims to provide a complete and easy to use Stacks API client implementation, thereby reducing the amount of boilerplate needed to launch a Stacks app.

Developers should be aware that on the back end, the Stacks API consists of two separate but related services:

1. The **Stacks Node** that exposes a JSON RPC API (these routes can be identified by the `/v2/` path.
2. The **Stacks Blockchain API **that proxies all the RPC API endpoints _and_ provides _extended_ endpoints for additional capabilities (these routes can be identified by the `/extended/` path.

In the client code and API examples within this document, we reference the Stacks API implementations freely hosted by [Hiro](https://hiro.so):

`mainnet: https://stacks-node-api.mainnet.stacks.co/`

`testnet: https://stacks-node-api.testnet.stacks.co/`

The hosted Stacks API offers a quick onboarding environment for developers to get started. To provide end users with a more trustless architecture, consider [hosting your own Stacks API](https://docs.hiro.so/get-started/running-api-node).

#### More resources

1. [https://docs.hiro.so/get-started/stacks-blockchain-api](https://docs.hiro.so/get-started/stacks-blockchain-api)
