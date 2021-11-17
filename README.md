# Getting started

### Introduction

`micro-stacks` is a library of JavaScript modules that enable you to interact with the Stacks ecosystem. The primary goals of this library are as follows:

* Core has no extra dependencies (just 2 dependencies: [noble-secp256k1](https://github.com/paulmillr/noble-secp256k1), [noble-hashes](https://github.com/paulmillr/noble-hashes)).
* Modular: take what you need, leave what you don't.
* ESM based, works with all modern bundlers.
* 100% deno compatible.
* Expo / React Native support.
* Un-opinionated core.
* Opinionated framework integrations.
* Use with wallet based authenticators.
* Highly typed -- written in typescript.
* Well tested.

### Installation

`micro-stacks` is a collection of different modules, each generally separate from each other. To install micro-stacks, you can use any JavaScript package manager you prefer.

{% tabs %}
{% tab title="pnpm" %}
```bash
pnpm add micro-stacks
```
{% endtab %}

{% tab title="yarn" %}
```bash
yarn add micro-stacks
```
{% endtab %}

{% tab title="npm" %}
```bash
npm install micro-stacks
```
{% endtab %}
{% endtabs %}

### Basic usage

```typescript
import { serializeCV } from 'micro-stacks/clarity';

const serialized = serializeCV(myClarityValue);

console.log(serialized)
```

### Modules

To learn more about all the modules that are included with micro-stacks, please continue to Module overview.

{% content-ref url="modules/core/" %}
[core](modules/core/)
{% endcontent-ref %}

### Framework integrations

`micro-stacks` also comes with highly opinionated framework integrations. Current, react is the only framework currently supported out of the box. You can still use all of the core modules of micro-stacks in any framework.

### React

The React integration is made up of three distinct packages:&#x20;

#### **@micro-stacks/react**

This package is the primary react integration. It has everything you need to build out complex stacks-based application.&#x20;

{% content-ref url="modules/frameworks/react/" %}
[react](modules/frameworks/react/)
{% endcontent-ref %}

#### **@micro-stacks/nextjs**

This package is made specifically to help build advanced next.js (SSR) stacks based applications.&#x20;

{% content-ref url="modules/frameworks/next.js.md" %}
[next.js.md](modules/frameworks/next.js.md)
{% endcontent-ref %}

#### **@micro-stacks/query**

This package is a highly opinionated abstraction on top of react-query and jotai, giving access to external stacks API data in a way that is very easy to use.

{% content-ref url="modules/frameworks/query.md" %}
[query.md](modules/frameworks/query.md)
{% endcontent-ref %}

To install any of them, follow the same steps as before:

{% tabs %}
{% tab title="pnpm" %}
```
pnpm install @micro-stacks/react @micro-stacks/nextjs @micro-stacks/query
```
{% endtab %}

{% tab title="yarn" %}
```
yarn add @micro-stacks/react @micro-stacks/nextjs @micro-stacks/query
```
{% endtab %}

{% tab title="npm" %}
```
npm add @micro-stacks/react @micro-stacks/nextjs @micro-stacks/query
```
{% endtab %}
{% endtabs %}

### Differences from stacks.js

`stacks.js` (previously known as `blockstack.js`) has years of use and maintenance behind it (which I have contributed towards), and it serves as a great foundation for building apps that use Gaia or interact with the Stacks Blockchain in some way. However, it has some (very well known and battle-tested) libraries that are huge in bundle-size which power its various cryptographic/blockchain functions. The most notable packages are: `elliptic`, `bitcoinjs-lib`, `bip39`, and `bn.js`.

Outside the libraries and dependencies that `stacks.js` has, there are long-standing, opinionated choices that have been made around how things should be used, mostly related to authentication and storage. I've spent years building ~~Block~~Stacks apps and `micro-stacks` is the culmination of my hopes and dreams when it comes to the future for building apps on the Stacks Blockchain.
