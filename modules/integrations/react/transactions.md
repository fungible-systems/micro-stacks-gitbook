# Transactions

Transaction signing will likely play a big role in the functionality of your app, especially if you need to interact with any smart contracts.

### useContractCall

```typescript
import { useContractCall } from '@micro-stacks/react';

const codeBody = `;; hello world`;
const contractName = 'foo bar';

const ContractDeployButton = () => {
  const { handleContractCall, isLoading } = useContractDeploy({
    contractAddress,
    contractName,
    functionName,
    functionArgs,
    postConditions
  });
  
  return <button onClick={handleContractCall}>
      {isLoading ? 'Loading...' : 'Call contract function'}
    </button>
};
```

### useContractDeploy

```typescript
import { useContractDeploy } from '@micro-stacks/react';

const codeBody = `;; hello world`;
const contractName = 'foo bar';

const ContractDeployButton = () => {
  const { handleContractDeploy, isLoading } = useContractDeploy({
    codeBody,
    contractName,
  });
  
  return <button onClick={handleContractDeploy}>
      {isLoading ? 'Loading...' : 'Deploy contract'}
    </button>
};
```

### useStxTransfer

```typescript
import { useStxTransfer } from '@micro-stacks/react';

const TokenTransferButton = ({recipient}: {recipient: string}) => {
  const { handleStxTransfer, isLoading } = useStxTransfer({
    recipient, 
    amount: 1 // amount in ustx (0.000001 STX)
  });
  
  return <button onClick={handleStxTransfer}>
      {isLoading ? 'Loading...' : 'Send STX'}
    </button>
};
```

###
