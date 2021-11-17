# Burnchain



### fetchBurnchainRewardSlotHolders

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchBurnchainRewardSlotHolders } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch burnchain reward slot holders
const holders = await fetchBurnchainRewardSlotHolders({
  url: network.getCoreApiUrl(),
  limit,
  offset,
});
```

This fetcher is a wrapper around the get burnchain reward slot holders endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/burnchain/reward_slot_holders" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchBurnchainRewardSlotHoldersByAddress

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchBurnchainRewardSlotHoldersByAddress } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch burnchain reward slot holders by address
const holders = await fetchBurnchainRewardSlotHoldersByAddress({
  url: network.getCoreApiUrl(),
  limit,
  offset,
  address,
});
```

This fetcher is a wrapper around the get burnchain reward slot holders by address endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/burnchain/reward_slot_holders/{address}" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchBurnchainRewards

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchBurnchainRewards } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch burnchain rewards
const rewards = await fetchBurnchainRewards({
  url: network.getCoreApiUrl(),
  limit,
  offset,
});
```

This fetcher is a wrapper around the get burnchain rewards endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/burnchain/rewards" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchBurnchainRewardsByAddress

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchBurnchainRewardsByAddress } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch burnchain rewards by address
const rewards = await fetchBurnchainRewardsByAddress({
  url: network.getCoreApiUrl(),
  limit,
  offset,
  address,
});
```

This fetcher is a wrapper around the get burnchain rewards by address endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/burnchain/rewards/{address}" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}

### fetchTotalBurnchainRewardsByAddress

```typescript
import { StacksMainnet } from 'micro-stacks/network';
import { fetchTotalBurnchainRewardsByAddress } from 'micro-stacks/api';

// example network
const network = new StacksMainnet()

// fetch total burnchain rewards by address
const total_rewards = await fetchTotalBurnchainRewardsByAddress({
  url: network.getCoreApiUrl(),
  address,
});
```

This fetcher is a wrapper around the get total burnchain rewards by address endpoint, described below:

{% swagger src="https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml" path="/extended/v1/burnchain/rewards/{address}/total" method="get" %}
[https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml](https://hirosystems.github.io/stacks-blockchain-api/openapi.resolved.yaml)
{% endswagger %}
