# Next.js

This package is a highly opinionated combination of `@micro-stacks/react` and `@micro-stacks/query` that makes use of [Jotai](https://jotai.org) for state management, and [`jotai-query-toolkit`](https://github.com/fungible-systems/jotai-query-toolkit) for all async data-fetching needs.&#x20;

## Getting started

To start out, `@micro-stacks/nextjs` exports a higher order component (HoC) that we must use to wrap each Next.js page. This is important because it allows us to set certain values automatically, such as a users session or other state elements.&#x20;

It's generally recommended to create a new file called `with-micro-stacks.ts` which exports your higher order component:

```typescript
import { wrapWithMicroStacks } from '@micro-stacks/nextjs';

export const withMicroStacks = wrapWithMicroStacks({
  authOptions: {
    appDetails: {
      name: 'test app',
      icon: 'icon',
    },
  },
});

```

You can then import this higher order component into each of your pages. Take this example Next.js page:

```tsx
import { WalletConnectButton } from '../components/wallet-connect-button';
import { withMicroStacks } from '../common/with-micro-stacks';

import type { NextPage } from 'next';

const Home: NextPage = () => {
  return (
    <div>
      <WalletConnectButton />
    </div>
  );
};

// wrap the default export
export default withMicroStacks(Home);
```

This now gives your app access to values from the `MicroStacksProvider`. Under-the-hood this is the same thing that you'd do in a client-side react application.

#### Help! I'm getting the error `No authOptions provided.` What do I do?

If you're getting this error but you've set everything up as described, it's likely due to some duplication of dependencies.&#x20;

You need to resolve to a single version of the dependencies. You can use this custom `next.config.js` file to resolve to only one version of each dependency:

```javascript
const path = require('path');

/** @type {import('next').NextConfig} */
module.exports = withBundleAnalyzer({
  reactStrictMode: true,
  webpack(config, { isServer }) {
    const fallback = config.resolve.fallback || (config.resolve.fallback = {});
    const alias = config.resolve.alias || (config.resolve.alias = {});

    // to make sure everything is using the same version of jotai and atoms in pkgs
    alias['jotai'] = path.resolve(__dirname, 'node_modules', 'jotai');
    alias['jotai-query-toolkit'] = path.resolve(__dirname, 'node_modules', 'jotai-query-toolkit');
    alias['react-query'] = path.resolve(__dirname, 'node_modules', 'react-query');
    alias['@micro-stacks/nextjs'] = path.resolve(__dirname, 'node_modules', '@micro-stacks/nextjs');
    alias['@micro-stacks/query'] = path.resolve(__dirname, 'node_modules', '@micro-stacks/query');
    alias['@micro-stacks/react'] = path.resolve(__dirname, 'node_modules', '@micro-stacks/react');
		
    // prevent some automatic polyfill next.js does
    if (!isServer) fallback['crypto'] = fallback['stream'] = false;
    return config;
  },
});
```

### Fetching data

One of the best features of Next.js (or any SSR app) is its ability to fetch data on the server and provide those results to the client on first load. With `@micro-stacks/nextjs` you can fetch certain data automatically, and have it be ready for your users on first load. Let's look at some examples:

```tsx
import { WalletConnectButton } from '../components/wallet-connect-button';
import { withMicroStacks } from '../common/with-micro-stacks';
import { makeGetServerSideProps } from '@micro-stacks/nextjs';

import type { NextPage } from 'next';

const Home: NextPage = () => {
  return (
    <div>
      <WalletConnectButton />
    </div>
  );
};

export const getServerSideProps = makeGetServerSideProps([
  'currentAccountBalances',
  'currentAccountTransactions',
  'currentAccountAssetsList',
]);

export default withMicroStacks(Home);
```
