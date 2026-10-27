# ETH Price

A [wedgie](https://wedgie.dev) app: the price of ETH, and the newest block on Ethereum and Base, every 30 seconds.

A wedgie has no internet. This app gets it from the computer it's plugged into: keep its page on wedgie.dev
open (wedgie.dev/connect, pick your wedgie), or run `python3 wedgie.py net`. It uses the firmware's `net`
module (firmware 0.3.61+). The sites it may reach are listed in `wedgie.json` under `"net"`:

- `"chain"`: read-only chain calls and the ETH price. First wedgie.dev's price (under 1 s, grey: it could be
  changed on the way), then Chainlink's, read over the wedgie's own TLS (firmware 0.3.70+: nobody in between can
  change it), then Ethereum's newest block the same way, Base's from wedgie.dev.

The screen: the price, big (grey till Chainlink's is in), and a check under it as each source confirms it:
Chainlink, then Coinbase. Down: a table of every number with its seconds and, under it (firmware 0.3.72+), every
step of the fetch under way: connect, keys made on the chip, encrypted, asked, each certificate checked, the
site's own signature, the answer. Up: back.
- `api.coinbase.com`: Coinbase's ETH price, to compare.

Green button: fetch now. How to write an app like it: https://wedgie.dev/code.md

MIT
