# Fees



### feesSearch

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { feesSearch } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch fees
const fees = await feesSearch({
  url: network.getCoreApiUrl(),
});
```

This fetcher is a wrapper around the get fees endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/v2/fees/transfer" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}
