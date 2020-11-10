---
title: Self-hosting RHOM payment processor
subtitle: BTCPayServer is a self-hosted, open-source cryptocurrency payment processor. It's secure, private, censorship-resistant and free
slug:
weight: 2
tags:
  - sellers
  - privacy
---

By hosting your own instance of Rhombus's BTCPayServer, you can create your very own independent payment processor for both Rhombus and Bitcoin.

{{< toc >}}

## About BTCPayServer

{{< vimeo 330290302 >}}

## Features

See [official BTCPayServer website](https://btcpayserver.org/) for complete info about features and abilities. To name a few:

- **No fees** – no processing/transaction fees or any 3rd-party eating up your profits
- **Peer to peer** – coins are sent directly from buyer to seller, they don't sit on the server itself (no middleman)
- **Multiple coins supported** – BTC (with optional Lightning), RHOM, LTC and more...
- **No KYC** – keep your identity to yourself
- **Self-hosted** – you're in control

## Available servers

Following BTCPayServer servers are run by the community and open for public, in case you don't want/need to run your own:

{{< hint alert >}}
**Sorry, no public BTCPayServers available at this time.** Maybe you might help out and host one yourself? :)
{{< /hint >}}

## Installation

For easier installation and management, `docker` images are available:

### Requirements

    docker
    docker-compose

### Generate docker-compose.yml

    git clone --depth=1 https://github.com/spazzymoto/btcpayserver-docker.git
    cd btcpayserver-docker
    export BTCPAYGEN_CRYPTO1="part"
    ./build.sh

**Note:** This will use Rhombus Core 0.18.0.6 RC1, if you wish to use the latest stable for mainnet just change the line in the `docker-compose.generated.yml`

    image: spazzymoto/rhombus:0.18.0.6rc1 -> image: spazzymoto/rhombus:0.17.1.4


### Run BTCPayServer

Still in `btcpayserver-docker` folder:

    cd Generated/
    export NBITCOIN_NETWORK="testnet"
    export BTCPAY_PROTOCOL="http"
    export BTCPAY_HOST="localhost"
    docker-compose -f docker-compose.generated.yml up

Go to `localhost` in your browser
