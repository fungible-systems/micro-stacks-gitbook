# Info

### fetchCoreApiInfo

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchCoreApiInfo } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch info
const info = await fetchCoreApiInfo({
  url: network.getCoreApiUrl(),
});
```

This fetcher is a wrapper around the get core api info endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/v2/info" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchStatus

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchStatus } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch status
const status = await fetchStatus({
  url: network.getCoreApiUrl(),
});
```

This fetcher is a wrapper around the get status endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/status" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchNetworkBlockTimes

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchNetworkBlockTimes } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch block_times
const block_times = await fetchNetworkBlockTimes({
  url: network.getCoreApiUrl(),
});
```

This fetcher is a wrapper around the get network block times endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/info/network_block_times" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchNetworkBlockTime

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchNetworkBlockTime } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch block_time
const fees = await fetchNetworkBlockTime({
  url: network.getCoreApiUrl(),
  network: 'mainnet',
});
```

This fetcher is a wrapper around the get network block time endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/info/network_block_time/{network}" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchStxSupply

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchStxSupply } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch fees
const supply = await fetchStxSupply({
  url: network.getCoreApiUrl(),
  height,
});
```

This fetcher is a wrapper around the get STX supply endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/stx_supply" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchStxSupplyPlain

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchStxSupplyPlain } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch supply
const supply = await fetchStxSupplyPlain({
  url: network.getCoreApiUrl(),
});
```

This fetcher is a wrapper around the get STX supply plain endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/stx_supply/total/plain" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchStxSupplyCirculatingPlain

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchStxSupplyCirculatingPlain } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch supply
const supply = await fetchStxSupplyCirculatingPlain({
  url: network.getCoreApiUrl(),
});
```

This fetcher is a wrapper around the get STX circulating supply plain endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/stx_supply/circulating/plain" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchStxSupplyLegacyFormat

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchStxSupplyLegacyFormat } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch supply
const supply = await fetchStxSupplyLegacyFormat({
  url: network.getCoreApiUrl(),
  height,
});
```

This fetcher is a wrapper around the get STX supply legacy endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/stx_supply/legacy_format" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchPox

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchPox } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch fees
const pox = await fetchPox({
  url: network.getCoreApiUrl(),
});
```

This fetcher is a wrapper around the get PoX endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/v2/pox" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}
