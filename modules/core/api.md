---
description: >-
  micro-stacks/api allows you to fetch data from the stacks-blockchain-api. It
  exports a set of fetchers that map to all available endpoints in the API.
---

# API

### `fetchAccountBalances`

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchAccountBalances } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch our balances
const balances = await fetchAccountBalances({
  url: network.getCoreApiUrl(),
  principal: '',
});
```

This fetcher is a wrapper around the get account balances endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/address/{principal}/balances" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}
