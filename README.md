<p align="left">
  <img alt="Barbotine Arbitrage System Logo" width="30%" height="30%" src="https://bas.teleporthq.app/playground_assets/bas-logo-rouge-200h.png">
</p>

[![Twitter @nelsodot](https://img.shields.io/twitter/url/https/twitter.com/nelsodot.svg?style=social&label=%20%40nelsodot)](https://twitter.com/nelsodot)
[![GitHub @nelso0](https://img.shields.io/github/followers/nelso0?label=follow&style=social)](https://github.com/nelso0)

More than a simple algorithm, [Barbotine Arbitrage System (B.A.S)](https://barbotine.capital) is a complete portfolio management system based on the price difference opportunities of the same asset on several centralized trading platforms.
To eliminate the risks and variables to be taken into account, **B.A.S operates without any transfer of assets between trading platforms.** It also operates in a delta-neutral situation, which brings it even closer to zero risk.

## Table of content
* [Features](#features)
* [Demo](#demo)
* [Prerequisites](#prerequis)
* [Installation](#installation)
* [Usage](#usage)
* [Contact](#contact)
* [Real version](#full-version)
<a name="features"/>
 
## Features

* True trading fees support
* Zero-risk (no speculation)
* Full live tracking on Telegram and Discord webhooks
* Permanent live rate display in the terminal
* Compatible with all [ccxt](https://github.com/ccxt/ccxt) exchanges simultaneously (multi-threading).

<a name="demo"/>
 
## Demo

* [See Barbotine running 24/7 on a $10,000 account on different crypto assets](https://barbotine.capital)

* [Youtube video demo](https://youtu.be/Hq7XXsiKJhI)

What an opportunity looks like (0 trading fees example):

![](https://media.discordapp.net/attachments/876447732259225612/1066487526807842836/demo_trades.gif)
In general, you can't know in advance how many opportunities there will be, and it's not constant at all. Plus, it also changes completely from one crypto to another. But I have observed that the more volatile the market is, the more opportunities there are.

<a name="prerequis"/>
 
## Prerequisites

The things you need before installing the software.

* Python 3
* Environment where you can run bash scripts (which means you can run bash scripts by typing ``bash <script.sh>`` in your terminal/cmd window. If you can't, go [here](https://www.thewindowsclub.com/how-to-run-sh-or-shell-script-file-in-windows-10))

<a name="installation"/>
 
## Installation

1. Clone the repository 
```sh
$ git clone https://github.com/nelso0/barbotine-arbitrage-bot # you can also download the zip file
```
2. Go to the repository you just cloned
```sh
$ cd barbotine-arbitrage-bot
```
3. Install all the requirements to run the arbitrage system
```sh
$ pip install -r requirements.txt
```
4. Put your 3 api keys and telegram bot details in [exchange_config.py](exchange_config.py)

5. Run and enjoy!

<a name="usage"/>
 
## Usage

Usage: 

```sh
$ bash main.sh <mode> <symbol-renew-time-minutes> <balance-usdt-to-use> {symbol}
```

* ```<mode>``` = the mode you wanna use among ```fake-money```, ```classic```, and ```delta-neutral```. 
  
  * ```fake-money``` will run the bot with the balance-usdt-to-use you put, with a virtual balance, just to test.
  * ```classic``` will run the bot with real USDT, and real profits.
  * ```delta-neutral```will run the bot with real USDT also, but in a delta-neutral situation. (a bit less profits but you won't loose a cent if the crypto you're using dump in 5 minutes (for very very careful people).
  
  
* ```<symbol-renew-time-minutes>``` = the timeframe you wanna use to switch symbol. If you put 60, it will renew the symbol each hour. Note that the new symbol is automatically selected by the [best_symbol.py](best-symbol.py) script if you don't put a {symbol}. Default: 15


* ```<balance-usdt-to-use>``` = how to be clearer? 


* ```{symbol}``` = Not mandatory. If you put a {symbol}, it will renew but on the same symbol every time. Every time it renews, it sells all the crypto and rebuy the crypto asset at the new price. 

Examples:

```sh
$ bash main.sh fake-money 15 500    # run the system with 500 USDT and renew symbol every 15 minutes.
```
```sh
$ bash main.sh classic 15 1000 SOL/USDT   # run the system with 1000 USDT on SOL/USDT continuously (change the symbol to SOL/USDT each 15 minutes).
```
```sh
$ bash main.sh delta-neutral 60 750   # run the system in a delta-neutral situation with 750 USDT and renew the symbol each hour. Note that with same amount of USDT, the delta-neutral mode will have 2/3 of the profits of the classic mode because it has less liquidity to invest in arbitrage opportunities.
```

## Contact

Discord: nelso#1800

Email: [nelso@barbotine.capital](mailto:nelso@barbotine.capital)

Don't forget to give a star if you like the code ⭐️

<a name="full-version"/>
 
## Full version

I also made a full version which operates with real dollars.
In general, the more volatile the crypto market, the more arbitrage opportunities there are - so the profits vary a lot from a month to another. I'm still doing my research on this, you can help me if you want! contact info below.

/!\ It's not a trading bot, it's an arbitrage bot, so you won't have trade losses at all, there is no speculation, Barbotine takes the opportunity only if it's profitable. /!\

[See live profits here.](https://barbotine.capital)

You can now buy the source code of that real version for a contribution of 25 bucks!

Link: [https://get.barbotine.capital](https://get.barbotine.capital/product/full-version-of-barbotine)
