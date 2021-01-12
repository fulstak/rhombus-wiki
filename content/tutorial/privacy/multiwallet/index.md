---
title: Running multiple wallets
subtitle: Separate your funds into multiple wallets, for different purposes
slug: multiwallet
weight: 1
tags:
  - multiwallet
  - privacy
---

{{< toc >}}

You might want to create and use multiple wallets for different usage. The goal is to separate your finances, so they won't mix up. This approach will also help you gain a bit [more privacy](/wiki/tutorial/privacy/tips/) (never linking all of your available funds).


## Multiwallet setup

### Rhombus Core

Same as on Bitcoin core wallet, launching multiple wallets on [Rhombus Core](/wiki/tutorial/wallets/rhombus-core/) is as easy as adding few `-wallet=` parameters - depending on your setup and location of your wallet files.

For example, if your wallets are in these locations:

```
.rhombus/
    primary-wallet.dat
    market/
        wallet.dat
    savings/
        wallet.dat
```

You would use these parameters:

```
$ rhombus-qt -wallet=primary-wallet.dat -wallet=market -wallet=savings
```

{{< image class="side-thumb" src="multiwallet-rhombus-qt.png" alt="Wallet switcher in Rhombus Core" >}}

Notice that for the `primary-wallet.dat` in the root folder, we added `.dat` to the parameter, which tells Rhombus Core that it's directly a wallet file, not its folder (as in case of `market/wallet.dat` and `savings/wallet.dat`).

This will open one Rhombus Core client with all 3 wallets loaded. You can then easily switch between them by choosing active wallet from the new dropdown (see screenshot).


## Autostart multiwallet

### Rhombus Desktop

{{< hint info >}}
**Rhombus Desktop launches with all available wallets loaded by default.**\
Therefore no extra configuration or setup is needed.
{{< /hint >}}

### Rhombus Core

#### Linux

Create a new custom application launcher in `~/.local/share/applications`:

```
$ nano ~/.local/share/applications/"Rhombus Core".desktop
```

Then paste and edit these lines (mainly `Exec=`) to match your setup:

```
#!/usr/bin/env xdg-open

[Desktop Entry]
Encoding=UTF-8
Name=Rhombus Core
GenericName=Rhombus Core
Comment=RHOM Wallet
Exec=/home/xxxxxx/rhombus/bin/rhombus-qt -wallet=xxxxxx.dat -wallet=xxxxxx
Terminal=false
Icon=rhombus
Keywords=Finance
Type=Application
Categories=Others
Name[en_US]=Rhombus Core
```

Save the changes via `CTRL-X` and then `Y`, confirm with `Enter`.