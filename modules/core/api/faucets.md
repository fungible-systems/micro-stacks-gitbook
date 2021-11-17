# Faucets



### fetchGetStxTokens

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchGetStxTokens } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch STX tokens
const tokens = await fetchGetStxTokens({
  url: network.getCoreApiUrl(),
  txid: '',
});
```

This fetcher is a wrapper around the get namespace price endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/faucets/stx" method="post" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchGetBtcTokens

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchGetBtcTokens } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch BTC tokens
const tokens = await fetchGetBtcTokens({
  url: network.getCoreApiUrl(),
  txid: '',
});
```

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/address/{principal}/balances" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}
