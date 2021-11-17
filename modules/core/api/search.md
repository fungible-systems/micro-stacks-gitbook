# Search

### fetchSearch

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchSearch } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch search
const search_results = await fetchSearch({
  url: network.getCoreApiUrl(),
  id: '',
});
```

This fetcher is a wrapper around the get search endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/search/{id}" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}
