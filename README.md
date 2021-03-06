# Maker Keeper Framework

Reference Maker Keeper Framework.

[![Build Status](https://travis-ci.org/makerdao/keeper.svg?branch=master)](https://travis-ci.org/makerdao/keeper)
[![codecov](https://codecov.io/gh/makerdao/keeper/branch/master/graph/badge.svg)](https://codecov.io/gh/makerdao/keeper)

## Rationale

The _SAI Stablecoin System_, as well as the _DAI Stablecoin System_ in the future,
both rely on external agents, often called keepers, to automate certain operations
around the Ethereum blockchain.

## Scope

This project covers three areas:
1. Provides a set of Python APIs to enable easy interaction with _SAI Stablecoin System_
   smart contracts and some other smart contracts surrounding it.
2. Provides some examples showing how to use these APIs.
3. Provides a basic set of keepers using these APIs aiming to keep liquidity of the system.

## Python APIs for Maker smart contracts

The current version provides APIs for `Tub`, `Lpc`, `ERC20Token`, `DSValue` and in addition
also for `SimpleMarket` (OasisDEX/OTC). There is also a working API around `AuctionManager`
and `SplittingAuctionManager`, but they will be used in _DAI Stablecoin System_, not in
_SAI Stablecoin System_.

You can find the full documentation here: http://maker-keeper-docs.surge.sh.
The documentation covers also examples and sample keepers provided.

**Beware!** This is the first version of the APIs and they will definitely change and/or evolve
in the future.

### Installation

The API and the keepers both use Python 3.6.1.

In order to install required third-party packages please execute:
```
pip install -r requirements.txt
```

In order for the requirements to install correctly on _macOS_, you may need to set
some environment variables:
```
export LDFLAGS="-L$(brew --prefix openssl)/lib" CFLAGS="-I$(brew --prefix openssl)/include" 
```

Also, installing `openssl` and `libtool` using Homebrew may help as well.
