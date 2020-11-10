---
title: Rhombus Open Marketplace
subtitle: Rhombus's Open Marketplace is a decentralized marketplace built with privacy at its core – it offers a low-cost, secure and scalable e-commerce experience 
slug: overview
weight: 1
tags:
  - market
  - important
aliases:
  - /learn/market/start
---

{{< toc >}}

## About Open Marketplace

> Buy and sell products and services from anyone else in the world without leaving a trail and using your favorite cryptocurrency.

**The Rhombus Open Marketplace is a hybrid between blockchain and peer-to-peer technologies.** It operates with no central authority or middleman and is exclusively owned and operated by its network of participants. Its decentralized nature enables new opportunities that cannot be offered by any other marketplace.

The Open Marketplace focuses on four core values: **privacy, security, scalability, and absolute decentralization**. It attains this goal by leveraging a combination of many different protocols. Each of these protocols contribute to Rhombus's core values in their own way.

{{< hint info >}}
**To access Rhombus Open Marketplace**\
follow our [Getting started with Open Marketplace](/tutorial/market/intro) guide!
{{< /hint >}}


## Features

{{< image class="side-thumb" src="rhombus-marketplace-infographic.jpg" alt="Open Marketplace infographic" >}}

> The Open Marketplace is private by default.

This means it automatically keeps users' identities and data private without requiring any extra step from the user. The only exception to that rule is the Tor setup which isn't enabled by default for security measures.

The Rhombus team is committed to only use the best privacy protocols the industry offers. It also constantly research, develop, and maintain the solutions deployed in the marketplace. As absolute privacy and security is the modus operandi of the project, it supersedes anything else. This means there is no concession made that would weaken the privacy setup of the marketplace in favor of something else.

### Payments

> All payments and transactions made on the Open Marketplace are untraceable by default.

This is achieved by leveraging the [Confidential Transactions (CT) and RingCT](/learn/transaction-types/) capabilities of the Rhombus coin (RHOM). These two protocols are integrated as the default types of payments, as specified by the [OMP](/learn/market/open-market-protocol/).

CT and RingCT transactions have been historically used on the Cryptonote codebase. Yet, the Rhombus team has adapted these protocols to be compatible with the Bitcoin codebase, which is the codebase used for the RHOM coin. The Bitcoin codebase gives more flexibility, security, and stability to the RHOM coin that the Cryptonote codebase would. A good example for this is the **ability for the RingCT and CT protocols to interact with smart-contracts** (i.e. the Open Marketplace). The coin also uses the Bulletproofs CT protocol improvement (currently on testnet) which reduces range proofs by about 70%. This ensures marketplace payments are both anonymous and scalable at the same time.

### Listings

**Public listings on Rhombus's Open Marketplace are listings that are publicly available.** Anyone can search for these listings using keywords and by navigating to the correct categories. Although these listings are public, they still offer a great level of privacy as all transactions are untraceable by default.

The only “identifiable” data public listings reveal is a unique and anonymous vendor ID. This ID cannot, however, link to any payment address or traceable identity.

{{< hint info >}}
**Rhombus Open Marketplace also offers Private listings** on users' "private markets", called [Private Bubbles](/learn/market/private-bubbles/)
{{< /hint >}}

### No metadata

> The Open Marketplace does not generate any sort of traceable data.

That much is true whether you are a buyer or a vendor. Metadata is “data about data” and can be very useful to track users. For example, pictures usually carry data such as the device used to take the picture, when it was taken, and even the precise geo-location of where the picture was taken. Any data stored off-chain on Rhombus's network is immediately stripped of all its metadata, making it impossible to trace people using metadata. This behavior is enabled by Rhombus's [SMSG Data Storage Network](/learn/market/smsg/).

### IP address anonymization

IP addresses can easily be anonymized on the Open Marketplace by [installing Tor and editing the configuration file](/tutorial/tor/) of your Rhombus Desktop client. Doing so shields you from getting your real IP address to be broadcast to the network.

**Rhombus Desktop currently doesn't automatically route connections through Tor for security measures.** If that were the case, a new Rhombus Desktop version would need to be installed by the user every time Tor pushes a new update. Automatic Tor updates, on the other hand, introduce severe security vulnerabilities, especially in regards to the authenticity of the files being automatically pushed to the client.

The Rhombus team is aware of a few solutions to circumvent this issue. It is also looking into alternatives to Tor. Automatic IP address anonymization should make their way onto Rhombus Desktop in the future.