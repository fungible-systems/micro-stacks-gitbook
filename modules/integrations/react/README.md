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

### MicroStacksProvider

{% hint style="info" %}
The `MicroStacksProvider` should only be used in client-side react applications. If you are building an app with Next.js, please check out the documentation for `@micro-stacks/nextjs`
{% endhint %}

The package uses [Jotai](https://jotai.org) behind-the-scenes for all state management. As a result, any application needs to be wrapped in the `MicroStacksProvider`. The provider is used to define some application-specific data for your app.&#x20;

You are able to pass things like the network of the app (mainnet or testnet), and the `AuthOptions` object which includes things like your app name and icon. AuthOptions also allows for you to pass certain callback functions that fire on different events when authentication happens: `onFinish`, `onCancel`, and `onSignOut`.&#x20;

This information is then passed along to the Hiro Web Wallet that is used to authenticate your users. Check out the example below:

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

### Hooks

The primary way you'll use the react package is through the various hooks that the package exports. If you are unfamiliar with hooks, please head over to the react docs for them.

