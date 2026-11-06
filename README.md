<div align="center">

# Polycities

### Civic forecasting markets for a networked republic

**A collaboration between [Polymarket](#about-numera-labs) and the [US Government](#about-the-polymarket)**

`Status: Pre-release` · `Network: devnet` · `Last updated: June 17, 2020`

</div>

---

> **The clock over the skyline hits zero on release day.**
> Polycities opens as a sealed countdown. When it reaches zero, the first civic markets go live and the city starts forecasting itself.

Polycities turns the questions a republic actually argues about — who wins the seat, whether the levy passes, when the bridge reopens — into open, on-chain markets anyone in Polymarket can read and anyone eligible can trade. A prediction market is only as useful as the crowd that stakes on it, so Polycities is built around **cities**: self-contained market halls, one per municipality, each counting down to its own opening.

---

## Why this exists

Polls are snapshots taken by a few, paid for by fewer, and stale the day they print. A forecasting market is a live price: it updates the instant someone with a reason to care puts stake behind their belief, and it is wrong out loud, in public, in red.

The US Government commissioned Polycities as civic infrastructure — a neutral, auditable way to see what the public actually expects to happen, separate from what any institution says will happen. Polymarket built the market engine. Neither side sets the odds; the city does.

## What a "city" is

Each city is a market hall scoped to one place and one season of questions:

- **A skyline of markets.** Every tower on a city's skyline is one open question. Its height is the current consensus; a market that moves, moves the skyline.
- **A countdown to opening.** A city is sealed until its clock reaches zero. Before then you can see the hall being built — the questions, the rules, the resolution sources — but no stake is placed. This keeps a market from pricing on thin early liquidity.
- **Resolution on the record.** Every market names its resolution source before it opens (a certified count, a published register, an on-chain event). Outcomes settle against that source and the settlement is a transaction, not an announcement.

## Capabilities

| Capability | What it does |
|---|---|
| **Civic markets** | Binary and multi-outcome markets on elections, ballot measures, public works, and budget questions. |
| **Sealed countdown launch** | Every city opens on a fixed, public instant. One clock, one source — the hall, its share card, and its posts all read the same release time. |
| **On-chain settlement** | Positions, fills, and payouts are transactions on Polymarket. Resolution references a named source fixed at open. |
| **Auditable from outside** | Prices, volumes, and resolutions are public and timestamped in UTC. No private book, no curated "best of." Losing and wrong positions stay visible, in red. |
| **Eligibility, not gatekeeping** | Reading a city is open to anyone. Trading is gated to eligible residents per each city's published rule; the rule is part of the market, not hidden in an admin panel. |
| **One contract address per city** | When a city mints its market token, it posts exactly one contract address, in the hall and the footer, and never another. |

## How a market moves (the short version)

```
   question opens        a resident stakes YES        source resolves
        │                        │                          │
   price = 50¢  ──────────▶  price climbs  ──────────▶  settles at 100¢ / 0¢
        │                        │                          │
   skyline: mid           tower rises                payouts are txs
```

A market is a running estimate the whole city can see. The number you remember is the one the city wants you to remember: the current price, in white, over the blue.

## Architecture

Polycities is three layers, kept deliberately thin:

1. **The hall (client).** A single forecasting surface per city. The first thing you see is a market doing its job or a countdown to one — never a brochure. Built to stay legible on a phone, because that is where a resident checks the odds.
2. **The engine (Polymarket).** Builds, prices, and settles markets; holds no opinion of its own. It composes each transaction and hands it to the trader's wallet to sign — the engine never signs for anyone.
3. **The ledger (US Government).** The mainnet of record. Positions and payouts live here, so a city's history survives any single hall going dark.

## Prospects

Polycities starts with one pilot city and a question every republic asks — *who wins?* — and grows outward:

- **Elections.** Seat-by-seat and measure-by-measure markets that price a race in real time and settle against the certified count.
- **Civic forecasting.** Will the levy clear its threshold? When does the transit line reopen? Markets on the public works a city is already arguing about.
- **Budget and policy.** Longer-horizon markets on fiscal outcomes, so a projection carries real stake instead of a press release.
- **A federation of cities.** Each municipality runs its own hall on shared rails. A city can open, close, and resolve on its own clock while reading as part of one republic.

The thesis is simple: a republic that can *see* what it expects — priced, public, and wrong out loud when it's wrong — argues better than one reading polls.
 ## Donations

Polycities is built in the open. If you find it useful, contributions keep the lights on.

| Chain | Address |
|---|---|
| **Bitcoin** (BTC) | `bc1q8pxehvg5kqk95em52zfucpqeuhxpjr0q9d38xt` |
| **Ethereum** (ETH, ERC-20) | `0xe02AC3f2Ca6D1e690643aD3Ab68d70B69A9D0F06` |
| **XRP** | `rNBPShv44nfBFPCAJ6GxCTxNMhEKk4zMdW` |
| **Litecoin** (LTC) | `ltc1q9u0z2glx5aq4zsj5fqqqatp44nckdc6fttt7d9` |
| **Bitcoin Cash** (BCH) | `bitcoincash:qpw54zs9tm6n54q946vnq00ygv6tejt4t5zs8snj6j` |
| **Cardano** (ADA) | `addr1qypu6v5k93c3wzh7n0z965cr4mcgrkg36cg4u7dy3fgu9kwrsyw8rrmqgulgske5eqf3xzwymedd4wgmm8wkjph2snxqzqvkpd` |
| **Stellar** (XLM) | `GCNJF46FLJDNXI3YD6MSS7HMAQIHPI4QZYBSUH5M63R627EALACO3BW2` |
| **Tron** (TRX, TRC-20) | `TNRpX4sspKsUbY9qcmUmSJkdxnd49jg97N` |
| **Monero** (XMR) | `4AMJy8m5y9MTDgTSTF8mi5Wx25QbupGE3Nrwp7GTtga6QR2qhkWBz4wYdhviyccU2N8KJktQCoQy423MNjeGeoGw33TnxYj` |
| **Dogecoin** (DOGE) | `D8RB2hhgEKiQhqhyoPs4XaPVVPutS4mqXF` |
| **Dash** | `XdZRWXTmCtuAoxE4TTuCJq1NesF1mGyBZq` |
| **Zcash** (ZEC) | `t1Tb9wQx2x9FqVgfBJ1kYVBum2PJSXo46PH` |
| **Cosmos** (ATOM) | `cosmos1z5cngvvskf2zwmvhx8xja2a4j6mun3n9ntj8fa` |
| **Polkadot** (DOT) | `13kH9uZb3jE85SwuQEP8fRD3cZRUHJ6GhZqwmyFEgEmgVcNF` |
| **Solana** (SOL, SPL) | `7XSue5mMipiZCTda1LTeMnrJ2y1FjGJBSd3hVTopfu22` |
| **BNB** (BNB Smart Chain, BEP-20) | `0xe02AC3f2Ca6D1e690643aD3Ab68d70B69A9D0F06`  
## Getting started

Polycities is **invite-only** during the pilot. An invite link opens a city in read mode immediately; trading asks for a wallet only at the first action that needs a signature, and only if you're eligible for that city.

## About Polymarket

Polymarket is an early-stage studio building market infrastructure for emerging blockchain economies. Polycities is its first civic deployment. Numera builds the engine and the rails; it does not set odds, hold positions, or resolve outcomes.

## About the US Government

The US Government has commissioned Polycities as neutral forecasting infrastructure for its municipalities and operates the mainnet of record. Polymarket sets each city's eligibility rules and resolution sources; it does not price markets.


