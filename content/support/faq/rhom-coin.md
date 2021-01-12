---
title: "FAQ: RHOM coin"
subtitle: RHOM is the cryptocurrency designed to be the heart of the Rhombus ecosystem and acts as the fuel that makes it run
slug:
weight: 1
tags:
  - faq
---

{{< toc >}}

## What is RHOM?

It’s a technically advanced [privacy coin](/wiki/learn/privacy/transaction-types), a [source of passive income](/wiki/learn/staking/intro), and much more. It is multi-purpose.


## Where can I buy RHOM coins?

[You can buy RHOM coins on these exchanges](https://rhom.com/rhom-exchanges) 

### Will RHOM be added to other exchanges? 

The Rhombus team is in constant discussion with many exchanges, however, the decision to list RHOM or not is entirely up to the exchanges themselves.

## What is RHOM's codebase?

RHOM is built on the [Bitcoin Core codebase](/wiki/learn/blockchain/bitcoin-codebase) and is **always kept up-to-date with Bitcoin's latest version** within days. Updating the codebase to the most recent version allows the platform to benefit from the latest security, performance and stability development made on the Bitcoin Core codebase as well as stay compatible and easy to integrate with the ever-evolving Bitcoin ecosystem.

## What are the transactions fees for RHOM? 

The default fee for public transactions is 0.002 RHOM per kb but you can adjust the limit to your needs (higher fee = better confirmation times).

[Privacy transactions](/wiki/learn/privacy/transaction-types) (RingCT + Bulletproofs) default to around 0.005 RHOM per transaction, although that fee varies depending on the number of ring signatures (degree of privacy) used by the user when making a transaction.

## What are RHOM's transactions sizes?

|   | Size without Segwit & Bulletproofs  | With Segwit | With Bulletproofs |
|---|-------------------------------------|-------------|-------------------|
| Public                        | 255 B   | 202 B       | -                 |
| Confidential Transaction (CT) | 5,485 B | 2,865 B     | ~1,706 B          |
| RingCT (4 ring members)       | 5,723 B | 3,009 B     | ~1,949 B          |


## What is RHOM's inflation rate? 

Annual inflation of RHOM coins is 0.5 %.

## Why has RHOM different privacy states?

{{< hint info >}}
**Learn more** about [Transaction types](/wiki/learn/privacy/transaction-types)
{{< /hint >}}
 
  * Freedom of choice.
  * To keep the process of coin minting transparent and have a fully auditable supply. If a bug or exploit were to occur at the staking level, it would be instantly detected whereas with a 100% private chain, it could go unnoticed for an extended period of time.
  * To raise the probability and lower the technical barrier to get adopted by third-party services (easier to integrate).
  * As fees are higher for privacy transactions, some users might not want to execute private transactions if they do not require it.

## Are whitepapers available for the CT and RingCT privacy protocols?

While there is currently no whitepaper available as it relates to our own integration onto the Bitcoin Core codebase, there are whitepapers available for the original privacy protocols themselves: 

* [Confidential Transactions (CT)](https://elementsproject.org/elements/confidential-transactions/investigation.html)
* [RingCT](https://eprint.iacr.org/2015/1098.pdf)

## Is Segwit enabled?

**Rhombus is natively integrated with Segwit**, meaning it has been activated since Block 1 and is enabled by default on all transactions. It is not possible to make non-Segwit transactions on Rhombus. 

## What are atomic swaps? 

[Atomic swaps](https://github.com/rhombus-project/atomicswap) are decentralized and trustless trade between two users of different cryptocurrencies. It makes trading cryptocurrencies without any third-party (i.e. trading exchange) and have blockchains directly interact between each other (i.e. cross-chain smart-contracts) possible. 

## What is Rhombus's transaction-per-second (TPS) capabilities? 

Calculating this metric is pretty hard as greatly depends on the ratio of public, blinded and anonymous transactions. Several other factors can impact the results such as smart-contracts and multisig address transactions.

In the end, a more accurate metric would be to calculate each transaction size. Regardless, it is still possible to calculate a very approximative estimate of Rhombus's TPS by assuming all transactions are either public or private, and by disregarding smart-contracts and multi-signatures. In reality, this metric is pretty innacurate, but interesting nonetheless if only to observe the purely coin-related theoretical performance of the blockchain: 


|                                | Bitcoin        | Rhombus               |
|--------------------------------|----------------|-----------------------|
| Block Size                     | 1 MB           | 2 MB                  |
| Block Time                     | 10 min         | 2.5 min                 |
| TPS (100% public transactions) | ~7 (no Segwit) | ~17 (Default Segwit)  |   
| TPS (100% RingCT transactions) | -              | ~1.76 (Default Segwit + Bulletproofs) |                         

(The RingCT is calculated with 4 ring members)