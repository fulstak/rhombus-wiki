---
title: How to stake
subtitle: Staking is a way of securing the Rhombus network (similar to “mining” in Bitcoin), while generating you passive income, or “interest”
slug: overview
weight: 1
tags:
  - staking
  - important
aliases:
  - /tutorial/staking/start
---

{{< toc >}}

To learn more in-depth about Rhombus's Staking feature, read [Rhombus Staking (intro)](/wiki/learn/staking/intro/).


## Staking methods

You can choose from few options on how to stake:

- **Standalone** – staking happens directly in your desktop wallet, your PC should be online ideally 24/7 (see below)
- **Staking on a Pool** – easily "pair" your desktop wallet with a [Staking Pool](/wiki/learn/staking/pools/); staking will happen automatically on pool
- **Staking on dedicated staking device (DSD)** – a fancy way to describe [staking on your own SBC](/wiki/learn/staking/dedicated-devices/) like Raspberry Pi or Rock64 without need to rely on third-party pool


## Comparison

| | Standalone | [Staking pools](/wiki/learn/staking/pools/) | [Dedicated staking devices](/wiki/learn/staking/dedicated-devices/) |
| ----------------------- |:------------------:|:---------:|:--------------------:|
| **Difficulty to setup** | easiest            | easy      | moderate             |
| **Staking happens**     | directly in wallet | on a pool | on dedicated device  |
| **Staking type**        | "hot" staking      | [Cold Staking](/wiki/learn/staking/intro#cold-staking/) | [Cold Staking](/wiki/learn/staking:#cold-staking) |
| **Fees**			          | –                  | 1–3 %     | –                    |
| **Security**			      | lower              | high      | high                 |
| **Howto guides**        | –                  | [setup guide](/wiki/tutorial/staking/cold-staking/) | [setup guide](/wiki/tutorial/staking/on-dedicated-device/) |

Standalone staking is easiest and fastest way to start staking. However as you can see, Pools and dedicated devices are more secure, so it's recommended to use those.


### Standalone staking

If you want to stake directly in your wallet (with [Rhombus Desktop](/wiki/tutorial/wallets/rhombus-desktop/) or [Rhombus Core](/wiki/tutorial/wallets/rhombus-core/)), you need to make sure, that:

- **Your wallet is unlocked.** You can check lock state by moving your mouse over the Lock icon in the bottom corner of your client. If your client is locked, click the icon and enter your password (you chose this password when you encrypted your wallet).
- **You have mature coins.** However weird that may sound, your coins need to mature first. When you withdraw coins from exchanges or receives them from friends, buyers, or from the escrow deal after a successful marketplace transaction, you'll need to wait at least 8 hours (225 confirmations) for them to mature. Only then they will stake. Keep in mind that first staking may be a bit longer than that – wait at least one day till you'll be getting regular staking rewards.
- **You have some public RHOM coins.** As described in [the comparison of currency types](/wiki/learn/privacy/transaction-types/), Anonymous and Blind RHOM coins don't stake. If you want stake rewards, be sure to have some public RHOM coins.
- **Have a decent amount of coins.** If you have less than ~1000 RHOM, you won't see staking rewards too often. Higher amounts of RHOM stake statistically more often.
- **Your wallet is open ideally 24/7.** Staking doesn't need a lot of electricity (as mining in PoW), but it needs some time. If your client is open just few hours a day, you might not see many staking rewards. For ideal results, keep you client open and staking 24/7. Dedicated staking devices (like Raspberry Pi or Pine64) are great way to achieve that without the need of having your main computer running all night.
- **You're in sync with the network.** This may be obvious, but you won't get any rewards during the time you sync your client with the network.

### Cold staking

{{< hint info >}}
**Refer to our unified [Cold Staking setup guide](/wiki/tutorial/staking/cold-staking/)**\
for details on how to setup staking on Pool or DSD
{{< /hint >}}
