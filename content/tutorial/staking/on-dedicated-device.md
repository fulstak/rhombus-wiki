---
title: Staking on DSD with Rhomtools
subtitle: DSD are ideal way for running Rhombus full node and getting staking rewards for securing the network 24/7
slug: 
weight: 3
tags:
  - staking
  - DSD
---

A Staking Node is a full blockchain node which has been configured to stake on behalf of your wallet (aka it has been delegated staking power over your wallet). The Staking Node is a computer running Rhombus that is always on and always connected to the internet. A Raspberry Pi 3 or comparable device (DSD) makes a perfect staking node as it consumes very little energy, is compact and easy to tailor for dedicated tasks.

{{< hint info >}}
Before you'll dive into this guide, **familiarize yourself with [Dedicated Staking Devices](/wiki/learn/staking/dedicated-devices/) and [Rhomtools utility](/wiki/learn/staking/rhomtools/)**.
{{< /hint >}}


## Requirements

Even though you could set up `rhombusd` for staking on your DSD manually, we'll focus on using Rhomtools staking utility, thanks to all the automation and ease of use it offers.

- **Rhombus wallet** – your primary wallet with funds on it ([Rhombus Core](/wiki/tutorial/wallets/rhombus-core/) or [Rhombus Copay](/wiki/tutorial/wallets/rhombus-copay/))
- **hardware for staking** – Raspberry Pi +3, Rock64 or other ("DSD")
  - older versions of RPi should work as well, but keep in mind that CPU performance does matter when staking, so you might not get ideal results
  - at least **32 GB of storage** (SD card)
  - **internet access** (wifi or cable) set up and working (follow guides for your device)
  - **SSH access** to device or connected monitor
  - **Debian/Ubuntu**-based OS (you can use any other distro, but you'll have to change following commands accordingly)

## Installation

{{< hint info >}}
**Visit [Rhomtools's Github repo](https://github.com/rhombus-project/rhomtools)** for more information if needed.
{{< /hint >}}

1. SSH to your device (or connect your monitor)
2. Make sure your system is up-to-date:

```bash
sudo apt update && sudo apt upgrade
```

### Install Rhomtools

Download Rhomtools and install its dependencies:

```bash
sudo apt-get install python git unzip pv jq dnsutils
cd ~ && git clone https://github.com/l0rdicon/rhomtools
```

Install Rhomtools:

```bash
cd rhomtools/
./rhomtools install
```

This will download, unzip and install the latest release Rhombus Core daemon (`rhombusd`).

Start `rhombusd` daemon:

```bash
./rhomtools restart now
```

Check `rhombusd` status and verify everything is running correctly (you might need to wait a minute or two, before `rhombusd` finishes starting up):

```bash
./rhomtools status
```

You should see a summary similar to this:

{{< image src="partyman-status.png" alt="Output of './rhomtools status' command" >}}

Great! Your node is now managed by Rhomtools and you have the latest `rhombusd` daemon running!


### Create a staking wallet

Generate a new wallet on the device by running:

```bash
./rhomtools stakingnode init
```

Follow instructions on screen to complete wallet setup.

{{< hint alert >}}
**Make sure you safely note node's [Recovery Phrase in a safe place](/wiki/tutorial/security/recovery-phrase/)!**\
This is the only key to your wallet in the unfortunate event that your device would got broken/stolen etc. Lose the key = lose the wallet!
{{< /hint >}}


### Generate staking public key

Next, we’ll create the public key which we will use within the Rhombus Desktop/Core to activate Cold Staking. We'll use Rhomtools utility for this as well.

To generate a new staking public key:

```bash
./rhomtools stakingnode new
```

Follow the directions to complete staking node public key creation. Public key label is just for you, so you know which key is connected to which wallet (in case you want to use multiple ones, e.g. staking on your desktop Rhombus Desktop _and_ your mobile Rhombus Copay).

You should see a Rhombus public key similar to this:

```
promKVAobLsHTQpZ5LzFHcZw8LD4sEEVuUdmcuAqCjDaaNJgypRmUUpFKMxbmn1hZ5V2J9SaG1QusCrngC9iiBAA8LvxVRx9aLBPjGeY4PtrxzW
```

And there's your staking public key! Make note of it somewhere, you'll need it later (friendly reminder that `CTRL+C` in Terminal doesn't copy text, so use your mouse's right-click instead).

### Summary

So far, we've achieved to:

- setup Rhomtools utility for managing your node via Rhomtools
- downloaded and autoconfigured latest Rhombus Core daemon on your device
- created a new Rhombus wallet on the device, dedicated to staking
- generated public key for staking (so that we can connect our main wallet to this DSD)

That concludes all the "tedious work" via Terminal on your Staking Node! Let's now move onto your main wallet and connect it with your Staking Node.

### Connect your wallet

{{< hint info >}}
To connect your wallet, **follow our unified [Cold staking setup](/wiki/tutorial/staking/cold-staking#connect-your-wallet) guide.**
{{< /hint >}}


## Maintenance

When your node is successfully set up, here are some tips to keep your node healthy and up-to-date.

### Updating rhombusd

**You should always keep your node up-to-date with latest Rhombus Core releases.**

To update your node:

1. SSH to your device (or connect your monitor)
2. Make sure your system is up-to-date: `sudo apt update && sudo apt upgrade`
3. To update rhomtools: `~/rhomtools/rhomtools update` and follow on-screen instructions
4. Wait a couple minutes for `rhombusd` to restart and check status of your node with `~/rhomtools/rhomtools status` - look for `rhombusd staking currently? : YES`

#### Updating to pre-release versions

In case you want to update your `rhombusd` to pre-release version (ie. betas, not yet stable releases), you can do so by:

```bash
cd ~/rhomtools/
git pull
./rhomtools update -prer
```

### Updating Rhomtools

In case rhomtools complains about updates available, you can install them simply by going to rhomtools directory and getting the latest code from GitHub:

```bash
cd ~/rhomtools/
git pull
```
