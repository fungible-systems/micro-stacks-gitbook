---
description: >-
  This page describes the different modules contained within the micro-stacks
  package.
---

# Core

Each module within `micro-stacks` can be safely imported without polluting your application with code from other modules. This allows for very high levels of tree-shakeability.

### Core modules

The core modules below are what make up the primary functionality that enables you to build Stacks based apps.

#### **API**

The API module `micro-stacks/api`, is the module that allows you to fetch data from the `stacks-blockchain-api`. It exports a set of fetchers that map to all available endpoints in the API.&#x20;

{% content-ref url="api/" %}
[api](api/)
{% endcontent-ref %}

#### **Clarity**

The `micro-stacks/clarity` module includes all the code required to interact with Clarity in a JavaScript environment. This includes things like parsing and constructing Clarity Values.&#x20;

{% content-ref url="clarity.md" %}
[clarity.md](clarity.md)
{% endcontent-ref %}

#### **Connect**

`micro-stacks/connect` is the module that handles all communication between a given application and any Stacks based wallet (currently only the Hiro Web Wallet is supported). This included functionality around authentication and signing transactions.&#x20;

{% content-ref url="connect/" %}
[connect](connect/)
{% endcontent-ref %}

#### **Crypto**

As the name implies, this module handles all of the crypto related functionality.

{% hint style="info" %}
#### Crypto extras

This package should generally not be used by most clients, however sometimes it might be required. This module is a set of crypto dependencies that might change in implementation depending on the environment.&#x20;
{% endhint %}

{% content-ref url="crypto.md" %}
[crypto.md](crypto.md)
{% endcontent-ref %}

#### **Network**

`micro-stacks/network` handles anything to do with constructing network objects related to Stacks.&#x20;

{% content-ref url="network.md" %}
[network.md](network.md)
{% endcontent-ref %}

#### **Storage**

This module is how you would interact with Gaia. It allows for you to safely store your users data encrypted.&#x20;

{% content-ref url="../integrations/react/storage.md" %}
[storage.md](../integrations/react/storage.md)
{% endcontent-ref %}

#### **Transactions**

This module deals with constructing Stacks Transactions that then can be signed by a given wallet.&#x20;

{% content-ref url="transactions.md" %}
[transactions.md](transactions.md)
{% endcontent-ref %}

### Extra modules

#### **Common**

This module exports helpful utilities that many of the other modules make use of.&#x20;

#### **BIP32**

This is a custom implementation of the BIP32 standard.&#x20;

#### **BIP39**

This is a custom implementation of the BIP39 standard.&#x20;

#### **Wallet SDK**

This module enables the creation of new Stacks wallet software.&#x20;

#### **Zone file**

This module deals with zone files, which are elements of BNS and Atlas.
