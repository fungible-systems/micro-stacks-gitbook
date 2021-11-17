# Microblocks



### fetchMicroblocks

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchMicroblocks } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch microblocks
const microblocks = await fetchMicroblocks({
  url: network.getCoreApiUrl(),
  limit,
  offset,
});
```

This fetcher is a wrapper around the get microblocks endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/microblock" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchMicroblock

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchMicroblock } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch microblock
const microblock = await fetchMicroblock({
  url: network.getCoreApiUrl(),
  hash: '',
});
```

This fetcher is a wrapper around the get microblock endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/microblock/{hash}" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchMicroblocksUnanchoredTransactions

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchMicroblocksUnanchoredTransactions } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch microblocks unanchored transactions
const unanchored_transactions = await fetchMicroblocksUnanchoredTransactions({
  url: network.getCoreApiUrl(),
});
```

This fetcher is a wrapper around the get microblocks unanchored transactions endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/microblock/unanchored/txs" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}
