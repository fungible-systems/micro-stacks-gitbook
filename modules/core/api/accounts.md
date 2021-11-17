# Accounts

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

### fetchAccountStxBalance

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchAccountStxBalance } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch stx balance
const stxBalance = await fetchAccountStxBalance({
  url: network.getCoreApiUrl(),
  principal: '',
});
```

This fetcher is a wrapper around the get STX account balance endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/address/{principal}/stx" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchAccountTransactions

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchAccountTransactions } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch account transactions
const stxBalance = await fetchAccountTransactions({
  url: network.getCoreApiUrl(),
  principal: '',
  limit = 20,
  offset = 0,
  height,
  unanchored, // TODO: unimplemented in micro-stacks
});
```

This fetcher is a wrapper around the get account transactions endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/address/{principal}/transactions" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchAccountTransactionsWithTransfers

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchAccountTransactionsWithTransfers } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch account transactions with stx transfers
const stxBalance = await fetchAccountTransactionsWithTransfers({
  url: network.getCoreApiUrl(),
  principal: '',
  limit = 20,
  offset = 0,
  height,
  unanchored, // TODO: unimplemented in micro-stacks
});
```

This fetcher is a wrapper around the get account transactions with STX transfers endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/address/{principal}/transactions_with_transfers" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchAccountAssets

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchAccountAssets } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch account assets
const stxBalance = await fetchAccountAssets({
  url: network.getCoreApiUrl(),
  principal: '',
  limit = 20,
  offset = 0,
  unanchored, // TODO: unimplemented in micro-stacks

});ty
```

This fetcher is a wrapper around the get account assets endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/address/{principal}/assets" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchAccountMempoolTransactions

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchAccountMempoolTransactions } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch account mempool transactions
const stxBalance = await fetchAccountMempoolTransactions({
  url: network.getCoreApiUrl(),
  principal: '',
  limit = 20,
  offset = 0,
});
```

This fetcher is a wrapper around the get account mempool transactions, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/tx/mempool" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

