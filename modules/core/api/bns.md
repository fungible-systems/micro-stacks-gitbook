# BNS



### fetchNamespacePrice

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchNamespacePrice } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch namespace price
const price = await fetchNamespacePrice({
  url: network.getCoreApiUrl(),
  tld: '',
});
```

This fetcher is a wrapper around the get namespace price endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/v2/prices/namespaces/{tld}" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchNamePrice

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchNamePrice } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch name price
const price = await fetchNamePrice({
  url: network.getCoreApiUrl(),
  name: '',
});
```

This fetcher is a wrapper around the get name price endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/v2/prices/names/{name}" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchNamespaces

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchNamespaces } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch namespaces
const namespaces = await fetchNamespaces({
  url: network.getCoreApiUrl(),
});
```

This fetcher is a wrapper around the get namespaces endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/v1/namespaces" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchNamesFromNamespaces

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchNamesFromNamespaces } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch names from namespace
const names = await fetchNamesFromNamespaces({
  url: network.getCoreApiUrl(),
  tld: '',
});
```

This fetcher is a wrapper around the get names from namespaces endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/v1/namespaces/{tld}/names" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchNames

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchNames } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch names
const names = await fetchNames({
  url: network.getCoreApiUrl(),
  page,
});types
```

This fetcher is a wrapper around the get names endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/v1/names" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchName

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchName } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch name
const name = await fetchName({
  url: network.getCoreApiUrl(),
  name: '',
});typesc
```

This fetcher is a wrapper around the get name endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/v1/names/{name}" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchNameHistory

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchNameHistory } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch name history
const history = await fetchNameHistory({
  url: network.getCoreApiUrl(),
  name: '',
});
```

This fetcher is a wrapper around the get name history endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/v1/names/{name}/history" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchZoneFile

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchZoneFile } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch zone_file
const zone_file = await fetchZoneFile({
  url: network.getCoreApiUrl(),
  name: '',
});
```

This fetcher is a wrapper around the get zone file endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/v1/names/{name}/zonefile" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchHistoricalZoneFile

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchHistoricalZoneFile } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch historical_zone_file
const historical_zone_file = await fetchHistoricalZoneFile({
  url: network.getCoreApiUrl(),
  name: '',
  zoneFileHash: '',
});
```

This fetcher is a wrapper around the get historical zone file endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/v1/names/{name}/zonefile/{zoneFileHash}" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchNamesByAddress

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchNamesByAddress } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch names by address
const names = await fetchNamesByAddress({
  url: network.getCoreApiUrl(),
  limckchainit,
  address,
});y
```

This fetcher is a wrapper around the get names by address endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/v1/addresses/{blockchain}/{address}" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchAllSubdomains

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchAllSubdomains } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch subdomains
const subdomains = await fetchAllSubdomains({
  url: network.getCoreApiUrl(),
  page,
});
```

This fetcher is a wrapper around the get subdomains endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/v1/subdomains" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchSubdomainAtTransaction

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchSubdomainAtTransaction } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch subdomain at transaction
const subdomain = await fetchSubdomainAtTransaction({
  url: network.getCoreApiUrl(),
  txid: '',
});
```

This fetcher is a wrapper around the get subdomain at transaction endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/v1/subdomains/{txid}" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}
