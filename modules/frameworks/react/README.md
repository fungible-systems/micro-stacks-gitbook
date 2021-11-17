---
description: >-
  This document outlines how to get started with micro-stacks in a react
  application.
---

# React

To get started, install the react package:

{% tabs %}
{% tab title="pnpm" %}
```
pnpm install @micro-stacks/react
```
{% endtab %}

{% tab title="yarn" %}
```
yarn add @micro-stacks/react
```
{% endtab %}

{% tab title="npm" %}
```
npm add @micro-stacks/react
```
{% endtab %}
{% endtabs %}

## MicroStacksProvider

{% hint style="info" %}
The `MicroStacksProvider` should only be used in client-side react applications. If you are building an app with Next.js, please check out the documentation for [`@micro-stacks/nextjs`](../next.js.md)``
{% endhint %}

The package uses [Jotai](https://jotai.org) behind-the-scenes for all state management. As a result, your application needs to be wrapped with `MicroStacksProvider`. The provider is used to define some micro-stacks specific data for your app.&#x20;

### AuthOptions

You are able to pass things like the network of the app (mainnet or testnet), and the `AuthOptions` object which includes things like your app name and icon. `AuthOptions` also allows for you to pass certain callback functions that fire on different events when authentication happens: `onFinish`, `onCancel`, and `onSignOut`.  Take a look at the TypeScript interface below to see all available options:

```typescript
interface AuthOptions {
  /** This callback is fired after authentication is finished. `StacksSessionState`: the data for the authenticated user */
  onFinish?: (payload: StacksSessionState) => void;
  /** This callback is fired if the user exits before finishing */
  onCancel?: (error?: Error) => void;
  /** This callback is fired when handleSignOut is called from the app */
  onSignOut?: () => void;
  scopes?: AuthScope[]; // see below
  appDetails: AppDetails; // see below
}

interface AppDetails {
  /** A human-readable name for your application */
  name: string;
  /** A full URL that resolves to an image icon for your application */
  icon: string;
}

type AuthScope =
  /**
   * Read and write data to the user's Gaia hub in an app-specific storage bucket.
   * This is the default scope.
   */
  | 'store_write'
  /**
   * Publish data so that other users of the app can discover and interact with the user.
   * The user's files stored on Gaia hub are made visible to others via the `apps` property in the
   * user’s `profile.json` file.
   */
  | 'publish_data';

```

This information is then passed along to the [Hiro Web Wallet](https://hiro.so/wallet/install-web) that is used to authenticate your users. Check out the example below:

```typescript
import { MicroStacksProvider } from '@micro-stacks/react';
import type { AuthOptions } from '@micro-stacks/react';

const authOptions: AuthOptions = {
  appDetails: {
    name: 'My cool app',
    icon: '/my-app-icon.png',
  }
}

const MyApp = () => {
  return <MicroStacksProvider authOptions={authOptions}>
    // rest of your app
  </MicroStacksProvider>
};
```

{% hint style="info" %}
**Important**: you should only define `MicroStacksProvider` once in your application, and you cannot use any nested `Providers` from Jotai.
{% endhint %}
