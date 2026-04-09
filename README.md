# Awesome TCG [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> The complete TCG Price Lookup developer ecosystem — APIs, SDKs, CLIs, and learning resources for building with live trading card prices across **Pokemon, Magic: The Gathering, Yu-Gi-Oh!, Disney Lorcana, One Piece TCG, Star Wars: Unlimited, and Flesh and Blood**.

[![Powered by TCG Price Lookup](https://img.shields.io/badge/powered%20by-TCG%20Price%20Lookup-purple.svg)](https://tcgpricelookup.com/tcg-api)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

One API. Every major trading card game. TCGPlayer market prices, eBay sold averages, and PSA / BGS / CGC graded comps — all in one place. This list indexes everything you need to build with the [TCG Price Lookup API](https://tcgpricelookup.com/tcg-api), from official SDKs in 5 languages to learning material and reference apps.

## Contents

- [The API](#the-api)
- [Official SDKs](#official-sdks)
- [Command-Line Tools](#command-line-tools)
- [Game Catalogs](#game-catalogs)
- [Code Examples](#code-examples)
- [Tools](#tools)
- [Learning Resources](#learning-resources)
- [Tutorials](#tutorials)
- [Reference Guides](#reference-guides)
- [Market Insights](#market-insights)
- [Listicles](#listicles)
- [Supported Games](#supported-games)

## The API

- **[TCG Price Lookup API](https://tcgpricelookup.com/tcg-api)** — One REST API for every major trading card game. TCGPlayer market prices, eBay sold averages, and graded card comps from PSA, BGS, CGC, SGC, ACE, and TAG.
  - **Free tier:** 10,000 requests/month, TCGPlayer market prices
  - **Trader plan and above:** eBay sold averages, full graded prices, 1-year price history
  - **Endpoints:** `/cards/search`, `/cards/{id}`, `/cards/{id}/history`, `/sets`, `/games`
  - **Auth:** API key via `X-API-Key` header
  - **Get a key:** <https://tcgpricelookup.com/tcg-api>

## Official SDKs

Native client libraries for every major language. Each SDK is a thin wrapper over the REST API with idiomatic conventions, typed errors, automatic batch chunking, and rate-limit headers.

- **[tcglookup-js](https://github.com/TCG-Price-Lookup/tcglookup-js)** — JavaScript / TypeScript SDK. Native `fetch`, ESM + CJS, zero runtime dependencies. Works in Node 18+, browsers, Bun, Deno, Cloudflare Workers.
  - npm: [`@tcgpricelookup/sdk`](https://www.npmjs.com/package/@tcgpricelookup/sdk)
- **[tcglookup-py](https://github.com/TCG-Price-Lookup/tcglookup-py)** — Python SDK built on httpx. Python 3.9+, sync API, context manager support.
  - PyPI: [`tcglookup`](https://pypi.org/project/tcglookup/)
- **[tcglookup-go](https://github.com/TCG-Price-Lookup/tcglookup-go)** — Go SDK with stdlib `net/http`. Functional options for configuration, typed error wrappers, no third-party dependencies.
  - Module: `github.com/TCG-Price-Lookup/tcglookup-go`
- **[tcglookup-rs](https://github.com/TCG-Price-Lookup/tcglookup-rs)** — Async Rust SDK built on reqwest + tokio. Builder pattern, typed error enum, fully documented on docs.rs.
  - crates.io: [`tcglookup`](https://crates.io/crates/tcglookup)
- **[tcglookup-php](https://github.com/TCG-Price-Lookup/tcglookup-php)** — PHP 8.1+ SDK built on Guzzle. PSR-4 autoloading, typed exception hierarchy.
  - Packagist: [`tcgpricelookup/sdk`](https://packagist.org/packages/tcgpricelookup/sdk)

## Command-Line Tools

- **[tcglookup CLI](https://github.com/TCG-Price-Lookup/tcglookup-cli)** — Terminal client for the TCG Price Lookup API. Search, lookup, and price-check cards from your shell. Built on the JS SDK.
  - npm: [`tcglookup`](https://www.npmjs.com/package/tcglookup)
  - Quick install: `npm i -g tcglookup && tcglookup search "blue-eyes white dragon"`

## Code Examples

- **[tcg-api-examples](https://github.com/TCG-Price-Lookup/tcg-api-examples)** — Runnable code samples for the API in **8 languages**: JavaScript, Python, Go, Rust, PHP, Ruby, Java, and C#. Each example covers search + get + rate-limit handling + typed error handling. Uses official SDKs where they exist; falls back to stdlib HTTP clients for languages without one.

## Game Catalogs

Live searchable catalogs for each supported game, backed by the same data the API returns.

- **[Pokemon](https://tcgpricelookup.com/pokemon)** — Pokemon TCG English catalog
- **[Pokemon Japan](https://tcgpricelookup.com/pokemon-japan)** — Japanese Pokemon TCG catalog
- **[Magic: The Gathering](https://tcgpricelookup.com/mtg)** — Complete MTG catalog including Reserved List
- **[Yu-Gi-Oh!](https://tcgpricelookup.com/yugioh)** — Every Yu-Gi-Oh! set from 1999 to today
- **[Disney Lorcana](https://tcgpricelookup.com/lorcana)** — Lorcana catalog with Enchanted rares
- **[One Piece TCG](https://tcgpricelookup.com/one-piece-card-game)** — One Piece English and Japanese
- **[Star Wars: Unlimited](https://tcgpricelookup.com/star-wars-unlimited)** — Full SWU catalog
- **[Flesh and Blood](https://tcgpricelookup.com/flesh-and-blood)** — Flesh and Blood with Cold Foil tracking

## Tools

- **[Card Catalog](https://tcgpricelookup.com/catalog)** — Cross-game search across every supported TCG
- **[Value Checker](https://tcgpricelookup.com/value-checker)** — Quick card value lookup tool
- **[Sets Browser](https://tcgpricelookup.com/sets)** — Browse every set across every game

## Learning Resources

The TCG Price Lookup blog covers tutorials, market insights, rarity guides, and game-specific reference content. Everything below is a free, in-depth article on tcgpricelookup.com.

### Tutorials

Hands-on guides for developers building with the API and collectors learning to value cards.

- **[How to Build a TCG Price Tracker in 50 Lines of TypeScript](https://tcgpricelookup.com/blog/build-tcg-price-tracker-javascript)** — End-to-end tutorial using `@tcgpricelookup/sdk`
- **[Building a Price Tracker with TCG API in 30 Minutes](https://tcgpricelookup.com/blog/build-price-tracker)** — Next.js + TCG API walkthrough
- **[How to Check Yu-Gi-Oh! Card Prices in 30 Seconds](https://tcgpricelookup.com/blog/yugioh-price-checker-30-seconds)** — Practical workflow for collectors
- **[How to Value a Trading Card Collection: Step-by-Step Guide](https://tcgpricelookup.com/blog/how-to-value-trading-card-collection)** — Complete collection valuation workflow

### Reference Guides

Definitive references on rarity, condition, and grading across the major TCGs.

- **[Trading Card Conditions Explained: Near Mint to Damaged](https://tcgpricelookup.com/blog/trading-card-conditions-explained)** — Universal condition guide
- **[PSA vs BGS vs CGC: The Complete Trading Card Grading Comparison](https://tcgpricelookup.com/blog/psa-vs-bgs-vs-cgc-complete-comparison)** — Grading service comparison
- **[Yu-Gi-Oh! Rarity Tiers Explained: Common to Quarter Century Secret Rare](https://tcgpricelookup.com/blog/yugioh-rarity-tiers-explained)** — Every Yu-Gi-Oh! rarity
- **[Disney Lorcana Rarity Tiers Explained](https://tcgpricelookup.com/blog/lorcana-rarity-tiers-explained)** — Lorcana rarity guide
- **[Star Wars: Unlimited Rarity Guide](https://tcgpricelookup.com/blog/star-wars-unlimited-rarity-guide)** — SWU rarity tiers including Hyperspace, Showcase, Prestige
- **[Disney Lorcana Enchanted Rares: Complete List](https://tcgpricelookup.com/blog/lorcana-enchanted-rares-list)** — Every Enchanted rare across every set
- **[Disney Lorcana Card Prices: How Much Is Yours Worth?](https://tcgpricelookup.com/blog/disney-lorcana-card-prices)** — Lorcana valuation guide
- **[Why eBay Sold Prices Matter More Than You Think](https://tcgpricelookup.com/blog/why-ebay-prices-matter)** — Price source comparison
- **[TCGPlayer vs eBay: Which Gives You the Most Accurate Card Prices?](https://tcgpricelookup.com/blog/tcgplayer-vs-ebay-card-prices)** — Marketplace comparison

### Market Insights

Analysis of game-specific markets, trends, and price drivers.

- **[Introducing TCG API: One API for Every Trading Card Game](https://tcgpricelookup.com/blog/introducing-tcg-api)** — API launch and positioning
- **[TCG Market Trends: Q1 2026 in Review](https://tcgpricelookup.com/blog/market-trends-q1-2026)** — Quarterly market commentary

### Game-Specific Price Guides

Comprehensive 2026 price guides for each major TCG.

- **[The Complete Yu-Gi-Oh! Card Price Guide for 2026](https://tcgpricelookup.com/blog/yugioh-card-price-guide-2026)** — Yu-Gi-Oh! valuation reference
- **[The Complete MTG Card Price Guide for 2026](https://tcgpricelookup.com/blog/mtg-card-price-guide-2026)** — Magic: The Gathering price guide
- **[The Complete One Piece TCG Price Guide for 2026](https://tcgpricelookup.com/blog/one-piece-tcg-price-guide-2026)** — One Piece TCG reference
- **[Disney Lorcana Price Guide 2026: Every Card, Every Set](https://tcgpricelookup.com/blog/disney-lorcana-price-guide-2026)** — Lorcana price guide
- **[Star Wars: Unlimited Price Guide 2026](https://tcgpricelookup.com/blog/star-wars-unlimited-price-guide-2026)** — SWU price guide
- **[Flesh and Blood Card Prices: The 2026 Complete Guide](https://tcgpricelookup.com/blog/flesh-and-blood-card-prices-2026)** — Flesh and Blood reference

### Listicles

Lists of the most valuable cards in each game with real sale data.

- **[The Most Expensive Pokemon Cards Ever Sold (2026)](https://tcgpricelookup.com/blog/most-expensive-pokemon-cards)** — Pokemon top sales
- **[The Most Expensive Yu-Gi-Oh! Cards Ever (2026)](https://tcgpricelookup.com/blog/most-expensive-yugioh-cards)** — Yu-Gi-Oh! top sales
- **[The Most Expensive MTG Cards Ever (2026)](https://tcgpricelookup.com/blog/most-expensive-mtg-cards)** — Magic top sales
- **[The Most Expensive One Piece TCG Cards Ever Sold (2026)](https://tcgpricelookup.com/blog/most-expensive-one-piece-cards)** — One Piece top sales
- **[The Most Expensive Disney Lorcana Cards Ever Sold (2026)](https://tcgpricelookup.com/blog/most-expensive-lorcana-cards)** — Lorcana top sales
- **[The Most Expensive Star Wars: Unlimited Cards (2026)](https://tcgpricelookup.com/blog/most-expensive-star-wars-unlimited-cards)** — SWU top sales
- **[The Most Expensive Flesh and Blood Cards Ever Sold (2026)](https://tcgpricelookup.com/blog/most-expensive-flesh-and-blood-cards)** — Flesh and Blood top sales
- **[How Much Is a Charizard Card Worth? Complete Price Guide (2026)](https://tcgpricelookup.com/blog/how-much-is-charizard-worth)** — Charizard variants reference

## Supported Games

The TCG Price Lookup API supports all major trading card games. Use these slugs in the `game` parameter of any API call:

| Slug | Game | Catalog |
|---|---|---|
| `pokemon` | Pokemon TCG (English) | [pokemon](https://tcgpricelookup.com/pokemon) |
| `pokemon-jp` | Pokemon TCG (Japanese) | [pokemon-japan](https://tcgpricelookup.com/pokemon-japan) |
| `mtg` | Magic: The Gathering | [mtg](https://tcgpricelookup.com/mtg) |
| `yugioh` | Yu-Gi-Oh! | [yugioh](https://tcgpricelookup.com/yugioh) |
| `lorcana` | Disney Lorcana | [lorcana](https://tcgpricelookup.com/lorcana) |
| `onepiece` | One Piece TCG | [one-piece-card-game](https://tcgpricelookup.com/one-piece-card-game) |
| `swu` | Star Wars: Unlimited | [star-wars-unlimited](https://tcgpricelookup.com/star-wars-unlimited) |
| `fab` | Flesh and Blood | [flesh-and-blood](https://tcgpricelookup.com/flesh-and-blood) |

## Quickstart Examples

### JavaScript / TypeScript

```ts
import { TcgLookupClient } from "@tcgpricelookup/sdk";

const client = new TcgLookupClient({ apiKey: "tlk_live_..." });
const results = await client.cards.search({ q: "charizard", game: "pokemon", limit: 5 });
```

### Python

```python
from tcglookup import TcgLookupClient

client = TcgLookupClient(api_key="tlk_live_...")
results = client.cards.search(q="charizard", game="pokemon", limit=5)
```

### Go

```go
import "github.com/TCG-Price-Lookup/tcglookup-go/tcglookup"

client := tcglookup.NewClient("tlk_live_...")
results, _ := client.Cards.Search(ctx, &tcglookup.CardSearchParams{
    Q: "charizard", Game: "pokemon", Limit: 5,
})
```

### Rust

```rust
use tcglookup::{Client, CardSearchParams};

let client = Client::new("tlk_live_...");
let results = client.cards().search(CardSearchParams {
    q: Some("charizard".into()),
    game: Some("pokemon".into()),
    limit: Some(5),
    ..Default::default()
}).await?;
```

### PHP

```php
use TcgPriceLookup\Client;

$client = new Client('tlk_live_...');
$results = $client->cards->search(['q' => 'charizard', 'game' => 'pokemon', 'limit' => 5]);
```

### CLI

```bash
tcglookup search "charizard" --game pokemon --limit 5
```

## Get Started

1. **Get a free API key** at [tcgpricelookup.com/tcg-api](https://tcgpricelookup.com/tcg-api)
2. **Pick your SDK** from the [Official SDKs](#official-sdks) section
3. **Run the quickstart** for your language above
4. **Build something** — see the [Tutorials](#tutorials) section for ideas

## License

This list is licensed under [MIT](LICENSE). All linked resources are owned and maintained by [TCG Price Lookup](https://tcgpricelookup.com).

---

Built and maintained by [TCG Price Lookup](https://tcgpricelookup.com). Get a free API key at [tcgpricelookup.com/tcg-api](https://tcgpricelookup.com/tcg-api).
