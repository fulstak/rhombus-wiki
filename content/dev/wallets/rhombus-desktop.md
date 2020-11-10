---
title: Rhombus Desktop
subtitle: Tips and notes for getting you up and running for Rhombus Desktop development in minutes 
slug:
weight: 1
tags:
  - dev
  - Rhombus Desktop
aliases:
  - /dev/rhombus-desktop
---

[Rhombus Desktop](/tutorial/wallets/rhombus-desktop) is Rhombus's flagship client/wallet for interacting with RHOM network.

{{< hint info >}}
**For latest development set up info**\
check [official repo of Rhombus Desktop](https://github.com/rhombus/rhombus-desktop) (on `dev` branch)
{{< /hint >}}

## Contribute

[![Snyk](https://snyk.io/test/github/rhombus/rhombus-desktop/badge.svg)](https://snyk.io/test/github/rhombus/rhombus-desktop)
[![Build Status](https://travis-ci.org/rhombus/rhombus-desktop.svg?branch=master)](https://travis-ci.org/rhombus/rhombus-desktop)
[![Coverage Status](https://coveralls.io/repos/github/rhombus/rhombus-desktop/badge.svg?branch=master)](https://coveralls.io/github/rhombus/rhombus-desktop?branch=master)
[![Code Climate](https://codeclimate.com/github/rhombus/rhombus-desktop/badges/gpa.svg)](https://codeclimate.com/github/rhombus/rhombus-desktop)
[![Greenkeeper badge](https://badges.greenkeeper.io/rhombus/rhombus-desktop.svg)](https://greenkeeper.io/)

Join us in [#rhombus-dev:matrix.org](https://app.element.io/#/room/#rhombus-dev:matrix.org) on [Element](https://element.io) (formerly Riot) for more info and/or assistance.

Keep in mind that the development currently happens on a private fork of this repo. 

## Requirements

* [Node.js®](https://nodejs.org/) v10
* [git](https://git-scm.com/)
* [yarn](https://yarnpkg.com/en/)

## Installation

Clone the repo & fetch dependencies:

```bash
git clone https://github.com/rhombus/rhombus-desktop
cd rhombus-desktop
yarn install
```

## Development

> Note: most recent development happens on `dev` branch

In project's folder:

1. Run `ng serve` to start the dev server and keep it running
1. In another terminal window, run `yarn run start:electron:dev -testnet --devtools` to start Rhombus Desktop on testnet (daemon will be updated and launched automatically)
   * `-testnet` – for running on testnet (omit for running the client on mainnet)
   * `-reindex` – reindexes the blockchain (in case you're stuck)
   * `--devtools` – automatically opens Developer Tools on client launch

### Interact with rhombus-core daemon

You can directly interact with the daemon ran by the Electron version:

```
./rhombus-cli -testnet getblockchaininfo
```

## Packaging

### Windows-only requirements

Building for Windows requires the 32-bit libraries to be available:

```
sudo apt-get install gcc-multilib
sudo apt-get install g++-multilib
```

### Packaging commands

* `yarn run package:win` – Windows
* `yarn run package:mac` – macOS
* `yarn run package:linux` – Linux


## Troubleshooting

### Development issues

#### Blockchain syncing stuck

Restart the app with `-reindex` flag:

```
yarn run start:electron:dev -testnet --devtools -reindex
```

### Other issues

See our [Rhombus Wiki](/support) for most common problems or join [#rhombushelp:matrix.org](https://app.element.io/#/room/#rhombushelp:matrix.org) on [Element](https://element.io) for community help.
