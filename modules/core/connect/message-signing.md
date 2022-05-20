---
description: Signed data (SIP-018)
---

# Message Signing

When interacting with the Stacks blockchain, much of the activity we do as users is considered "signing" messages. What this means is that we are using our private keys to verify that some bits of data are really something we want to do. This is most often in the form of signing and then broadcasting transactions. However, there are many use cases for which we'd want to sign something that is _not_ a transaction. Taken from the SIP-018 introduction:

> Digital signatures are at the heart of blockchains. They allow users to transfer assets, invoke smart contracts and more, without a designated trusted third party. To perform these actions, a user signs a transaction and broadcasts it to the network. However, there are situations in which it is desirable to produce signed messages that are not transactions.
>
> 1. prove to an external application or entity that a user is in control of an address;
> 2. authorize an action to be performed by a smart contract at a later stage (like a meta transaction, see below);
> 3. participate in an off-chain mechanism that is later settled on-chain (like a subnet).
>
> It is important that signed messages are understandable for humans. For transactions, this is obvious: wallet applications display whom is receiving how many tokens of what kind. Likewise, the input parameters, function name, and target contract of contract calls are properly listed. Signed messages that are not transactions should be no different.

Typically a Stacks-based app will not be responsible for any private keys, but instead something like the Hiro Web Wallet or Xverse will be the application that ends up signing messages.&#x20;

`micro-stacks/connect` exports a number of helper methods to work with these wallets to send requests for them to ultimately sign.&#x20;

{% hint style="info" %}
These methods are typically implemented via framework specific packages, such as `@micro-stacks/react`
{% endhint %}

### handleSignMessageRequest

This is the function for sending a standard string message to the wallet for signing. This is different than the Structured Data standard as described in SIP-018.

This method takes these options:

```typescript
export interface SignatureRequestOptions {
  message: string;
  appDetails: AuthOptions['appDetails'];
  authOrigin?: string;
  stxAddress: string;
  privateKey: string;
  network?: StacksNetwork;
}
// with optional callbacks to fire when the action is complete
// or when it has been canceled
export type SignedOptionsWithOnHandlers<T> = T & {
  onFinish?: (payload: SignatureData) => void;
  onCancel?: (errorMessage?: string) => void;
};
```

Here is an example of how you would call this function:

```typescript
import { handleSignMessageRequest } from 'micro-stacks/connect';
import { privateKeyToStxAddress } from 'micro-stacks/crypto';

async function openSignatureRequest() {
  // random private key
  const privateKey = '82db81f7710be42e5bbbab151801d41101c0af55f3b772cbaeae80cab7bd5b8f';
  const stxAddress = privateKeyToStxAddress(privateKey);

  await handleSignMessageRequest({
    privateKey,
    stxAddress,
    message: 'hello world',
    appDetails: {
      name: 'some test app',
      icon: 'icon',
    },
    onFinish(payload) {
      console.log(payload);
    },
    onCancel() {
      console.log('canceled!');
    },
  });
}
```

### handleSignStructuredDataRequest

This method is basically the same as the one described above, however the `message` value that it expects is either a hex-encoded `ClarityValue`, or a `ClarityValue` type.

```typescript
// the type is the same, but the message is different
export type StructuredSignatureRequestOptions = Omit<SignatureRequestOptions, 'message'> & {
  message: string | ClarityValue;
};
// it has the same onFinish and onCancel signatures as above.
```

And here is an example of how you can call this:

```typescript
import { handleSignStructuredDataRequest } from 'micro-stacks/connect';
import { privateKeyToStxAddress } from 'micro-stacks/crypto';
import { tupleCV, stringAsciiCV, cvToHex } from 'micro-stacks/clarity';

async function openStructuredDataSignatureRequest() {
  // random private key
  const privateKey = '82db81f7710be42e5bbbab151801d41101c0af55f3b772cbaeae80cab7bd5b8f';
  const stxAddress = privateKeyToStxAddress(privateKey);
  
  // can use either of these
  const message = tupleCV({ hello: stringAsciiCV('world') });
  const hexEncoded = cvToHex(message);

  await handleSignStructuredDataRequest({
    privateKey,
    stxAddress,
    message,
    appDetails: {
      name: 'some test app',
      icon: 'icon',
    },
    onFinish(payload) {
      console.log(payload);
    },
    onCancel() {
      console.log('canceled!');
    },
  });
}
```

### Verification

Okay, now that you've sent some messages to get signed, you want to verify that the signatures are owned by a given address, right?

There are a few options we have for how we want to validate these messages. The payload that the wallets return should include two things: `signature` and `publicKey`. The type of signature that the wallets return should be one that is considered a "Recoverable Signature". This means the signature contains enough data within it so that you are able to extract the publicKey that was used to sign this message! cool huh.

### verifyMessageSignature

This is the primary method we use to validate a signature.

```typescript
import { tupleCV, cvToHex, uintCV } from 'micro-stacks/clarity';

const payload = {
  signature: '007db2f251643ff11493ae377db2581a55b5dcce11a9b79becc177dc97a2fb6932076bd197a8e3772eab317d95a1c78f60adfcbf8e1512357c3f95d6606ad7dd29',
  publicKey: '035b08fd4d14786187f51a3360864665fa437a9ad22bbdf7ae716d4599f26943a7',
};
const message = cvToHex(tupleCV({ hello: uintCV(100) })).replace('0x', '');

// we can recover the publicKey
const isValid = verifyMessageSignature({ message, signature: payload.signature })

// or we can pass it too
const isValid = verifyMessageSignature({ message, signature: payload.signature, publicKey: payload.publicKey })
```
