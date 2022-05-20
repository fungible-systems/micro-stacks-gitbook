# Post Conditions

Post conditions add sanity checks for a well defined expected outcome for STX, Fungible and Non-Fungible token transfers that a user can easily view before signing a transaction. Here are examples of each type.&#x20;

#### Imports, etc.

```typescript
import { stringUtf8CV } from 'micro-stacks/clarity';
import {
  PostConditionMode,
  createSTXPostCondition,
  createNonFungiblePostCondition,
  FungibleConditionCode,
  NonFungibleConditionCode,
  createAssetInfo
} from 'micro-stacks/transactions';
import { networkAtom, userStxAddressesAtom, useTransactionPopup } from '@micro-stacks/react';
import { ChainID } from 'micro-stacks/common';

[...]

  const [contractAddress, contractName] = myContract.split('.');
  const [network] = useAtom(networkAtom);
  const amount = 1000000n;
  const chain = network?.chainId === ChainID.Mainnet ? 'mainnet' : 'testnet';
  const [userStxAddresses] = useAtom(userStxAddressesAtom);
  const userStxAddress = userStxAddresses?.[chain] || contractAddress;
  const { handleContractCall } = useTransactionPopup();
  
[...]

  handleContractCall({
    contractAddress,
    contractName,
    functionName: 'my-function',
    functionArgs: [],
    postConditionMode: PostConditionMode.Deny,
    postConditions: [stxPostCond, nftPostCond],
    onFinish,
    onCancel,
  });
```

### STX Post Condition

#### With Standard Principal

```typescript
const stxPostCond = createSTXPostCondition(
    userStxAddress,
    FungibleConditionCode.Equal, 
    amount
);
```

#### With Contract Principal

### Fungible Token Post Condition

#### With Standard Principal

#### With Contract Principal

### Non-Fungible Token Post Condition

#### With Standard Principal

```typescript
const nftPostCond = createNonFungiblePostCondition(
    userStxAddress,
    NonFungibleConditionCode.Owns,
    createAssetInfo(contractAddress, contractName, 'MY-NFT'),
    stringUtf8CV('MY-NFT')
);
```

#### With Contract Principal
