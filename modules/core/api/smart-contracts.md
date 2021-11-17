# Smart Contracts



### fetchContractById

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchContractById } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch contract by contract_id
const contract = await fetchContractById({
  url: network.getCoreApiUrl(),
  contract_id,
  unanchored,
});
```

This fetcher is a wrapper around the get contract by contract\_id endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/contract/{contract_id}" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchContractEventsById

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchContractEventsById } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch contract events by contract_id
const events = await fetchContractEventsById({
  url: network.getCoreApiUrl(),
  contract_id,
  limit,
  offset,
  unanchored,
});
```

This fetcher is a wrapper around the get contract events by contract\_id endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/contract/{contract_id}/events" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchContractInterface

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchContractInterface } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch contract interface
const contract_interface = await fetchContractInterface({
  url: network.getCoreApiUrl(),
  contract_address,
  contract_name,
  tip,
});
```

This fetcher is a wrapper around the get contract interface endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/v2/contracts/interface/{contract_address}/{contract_name}" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchContractDataMapEntry

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchContractDataMapEntry } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch contract data map entry
const data_map_entry = await fetchContractDataMapEntry({
  url: network.getCoreApiUrl(),
  contract_name,
  contract_address,
  map_name,
  proof,
  tip,
  lookup_key,
});
```

This fetcher is a wrapper around the post contract data\_map entry endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/v2/map_entry/{contract_address}/{contract_name}/{map_name}" method="post" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchContractSource

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchContractSource } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch contract_source
const contract_source = await fetchContractSource({
  url: network.getCoreApiUrl(),
  contract_address,
  contract_name,
  proof,
  tip,
});
```

This fetcher is a wrapper around the get contract source endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/v2/contracts/source/{contract_address}/{contract_name}" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchReadOnlyFunction

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchReadOnlyFunction } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch read only function
const read_only_function = await fetchReadOnlyFunction({
  url: network.getCoreApiUrl(),
  contractAddress,
  contractName,
  functionArgs,
  sender = contractAddress,
  functionName,
  tip,
});
```

This fetcher is a wrapper around the post read only function endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/v2/contracts/call-read/{contract_address}/{contract_name}/{function_name}" method="post" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}
