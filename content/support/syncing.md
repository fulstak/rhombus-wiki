---
title: Fixing syncing issues
subtitle: Are you having trouble synchronizing latest blocks? 
slug:
weight: 1
tags:
  - support
  - TODO
---

Rhombus wallets are a network-based software. **Make sure that no firewall or anti-virus software is blocking Rhombus from running or connecting the internet**. If in doubt, disable them for testing purposes and enable them afterwards if you have identified your problem.

## Update to latest version

Make sure you're running on [latest version](https://rhom.com/downloads).

If not, update your wallet.

## Reindex blockchain

Relaunch the client with `-reindex` flag:

{{< tabs "reindex" >}}

{{< tab "Windows" >}}
### Windows

- **Rhombus Core**: FIXME
{{< /tab >}}

{{< tab "macOS" >}}
### macOS

- **Rhombus Desktop**: launch via `/rhombus-desktop.app/Contents/MacOS/rhombus-desktop -reindex` on actual Rhombus Desktop binary
- **Rhombus Core**: FIXME
{{< /tab >}}

{{< tab "Linux" >}}
### Linux

- **Rhombus Core**: launch wallet via `./rhombus-qt -reindex` in app directory
{{< /tab >}}

{{< /tabs >}}
