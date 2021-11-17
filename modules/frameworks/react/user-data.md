---
description: >-
  This document describes what user data is available during an active session
  and how to use it.
---

# User data

After your users have authenticated via their wallet, your application can now use data specific to them. This data includes things like their Stacks addresses, decentralized identity hash, and their App Private Key.&#x20;

### useUser

This will likely be your most used hook when wanting to retrieve any user specific data. This hook will return the type `StacksSessionData` with an additional key of `currentStxAddress`

```typescript
interface UserData {
    currentStxAddress?: string;
    addresses: {
        testnet: string;
        mainnet: string;
    };
    appPrivateKey: string;
    associationToken: string;
    hubUrl: string;
    public_keys?: string[];
    profile: Profile;
    profile_url: string;
    username: string | null;
    version?: string;
    decentralizedID: string;
    identityAddress?: string;
}
```

### Additional hooks

There are some useful hooks for elements of data we might care about, such as `useCurrentStxAddress`. See the examples below for the other hooks:

#### useCurrentStxAddress

This one is pretty straightforward -- it will return the current version of the users address: mainnet or testnet.

#### useIsSignedIn

This is a small helper hook to only provide if a user is currently signed in or not.

####
