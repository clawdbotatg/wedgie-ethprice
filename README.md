# ETH Price

A [wedgie](https://wedgie.dev) app: the price of ETH, and the newest block on Ethereum and Base, every 30 seconds.

A wedgie has no internet. This app gets it from the computer it's plugged into: keep its page on wedgie.dev
open (wedgie.dev/connect, pick your wedgie), or run `python3 wedgie.py net`. It uses the firmware's `net`
module (firmware 0.3.61+). The sites it may reach are listed in `wedgie.json` under `"net"`:

- `"chain"`: read-only chain calls and the ETH price, through wedgie.dev (its Alchemy key stays there).
- `api.coinbase.com`: Coinbase's ETH price, to compare.

Green button: fetch now. How to write an app like it: https://wedgie.dev/code.md

MIT
