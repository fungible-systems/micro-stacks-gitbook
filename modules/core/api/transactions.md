# Transactions

### fetchTransactionsList

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchTransactionsList } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch transactions
const transactions = await fetchTransactionsList({
  url: network.getCoreApiUrl(),
  limit,
  offset,
  type,
});
```

This fetcher is a wrapper around the get transactions endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/tx" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchMempoolTransactionsList

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchMempoolTransactionsList } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch mempool transactions
const mempool_transactions = await fetchMempoolTransactionsList({
  url: network.getCoreApiUrl(),
  limit,
  offset,
  sender_address,
  recipient_address,
  address,
});
```

This fetcher is a wrapper around the get mempool transactions endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/tx/mempool" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchDroppedMempoolTransactionsList

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchDroppedMempoolTransactionsList } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch dropped mempool transactions
const dropped_mempool_transactions = await fetchDroppedMempoolTransactionsList({
  url: network.getCoreApiUrl(),
  limit,
  offset,
});
```

This fetcher is a wrapper around the get dropped mempool transactions endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/tx/mempool/dropped" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchTransaction

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchTransaction } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch transaction
const transaction = await fetchTransaction({
  url: network.getCoreApiUrl(),
  txid,
  event_offset,
  event_limit,
});
```

This fetcher is a wrapper around the get transaction endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/tx/{tx_id}" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchRawTransaction

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchRawTransaction } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch raw transaction
const raw_transaction = await fetchRawTransaction({
  url: network.getCoreApiUrl(),
  txid: '',
});
```

This fetcher is a wrapper around the get raw transaction endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/tx/{tx_id}/raw" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchTransactionsByBlockHash

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchTransactionsByBlockHash } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch transactions by block_hash
const transactions = await fetchTransactionsByBlockHash({
  url: network.getCoreApiUrl(),
  block_hash,
  limit,
  offset,
});
```

This fetcher is a wrapper around the get transaction by block\_hash endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/tx/block/{block_hash}" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchTransactionsByBlockHeight

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchTransactionsByBlockHeight } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch transactions by block_height
const subdomain = await fetchTransactionsByBlockHeight({
  url: network.getCoreApiUrl(),
  block_height,
  limit,
  offset,
});
```

This fetcher is a wrapper around the get transactions by block\_height endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/tx/block_height/{height}" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}
