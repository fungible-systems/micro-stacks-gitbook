# Tokens

### fetchFtMetadataList

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchFtMetadataList } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch FT metadata list
const ft_metadata_list = await fetchFtMetadataList({
  url: network.getCoreApiUrl(),
});
```

This fetcher is a wrapper around the get FT metadata endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/tokens/ft/metadata" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchNftMetadataList

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchNftMetadataList } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch NFT metadata list
const nft_metadata_list = await fetchNftMetadataList({
  url: network.getCoreApiUrl(),
});
```

This fetcher is a wrapper around the get NFT metadata endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/tokens/nft/metadata" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchNftMetadataForContractId

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchNftMetadataForContractId } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch NFT metadata for contract_id
const nft_metadata = await fetchNftMetadataForContractId({
  url: network.getCoreApiUrl(),
  contractId: '',
});
```

This fetcher is a wrapper around the get NFT metadata for contract\_id endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/tokens/{contractId}/nft/metadata" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchFtMetadataForContractId

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchFtMetadataForContractId } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch FT metadata for contract_id
const ft_metadata = await fetchFtMetadataForContractId({
  url: network.getCoreApiUrl(),
  contractId: '',
});
```

This fetcher is a wrapper around the get FT metadata for contract\_id endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/tokens/{contractId}/ft/metadata" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}
