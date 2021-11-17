# Blocks

### fetchBlocks

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchBlocks } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch blocks
const blocks = await fetchBlocks({
  url: network.getCoreApiUrl(),
  limit,
  offset,
});
```

This fetcher is a wrapper around the get blocks endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/block" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchBlock

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchBlock } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch block
const block = await fetchBlock({
  url: network.getCoreApiUrl(),
  hash: '',
});
```

This fetcher is a wrapper around the get account balances endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/block/{hash}" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchBlockByHeight

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchBlockByHeight } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch block by height
const block = await fetchBlockByHeight({
  url: network.getCoreApiUrl(),
  height,
});
```

This fetcher is a wrapper around the get account balances endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/block/by_height/{height}" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchBlockByBurnBlockHash

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchBlockByBurnBlockHash } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch block by burn_block_hash
const block = await fetchBlockByBurnBlockHash({
  url: network.getCoreApiUrl(),
  burn_block_hash: '',
});
```

This fetcher is a wrapper around the get account balances endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/block/by_burn_block_hash/{burn_block_hash}" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchBlockByBurnBlockHeight

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchBlockByBurnBlockHeight } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch block by burn_block_height
const block = await fetchBlockByBurnBlockHeight({
  url: network.getCoreApiUrl(),
  burn_block_height,
});
```

This fetcher is a wrapper around the get account balances endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/block/by_burn_block_height/{burn_block_height}" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}
