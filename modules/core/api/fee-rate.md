# Fee Rate



### fetchFeeRate

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchFeeRate } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch fee_rate
const fee_rate = await fetchFeeRate({
  url: network.getCoreApiUrl(),
  transaction: '',
});
```

This fetcher is a wrapper around the get fee rate endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/fee_rate" method="post" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}
