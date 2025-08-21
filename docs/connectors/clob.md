CLOB (Central Limit Order Book) connectors integrate into a CLOB exchange's WebSocket API, enabling standardized order placement/cancellation and order book data fetching from the perspective of Hummingbot strategies. These connectors work with both centralized exchanges (CEX) and decentralized exchanges (DEX) that utilize a central limit order book model. 

Each connector is customized for a particular exchange's idiosyncrasies to enable this level of standardization, so they should ideally have a maintainer, whose role is to ensure consistent performance by fixing bugs, incorporating API updates, and other ongoing work.

### CLOB Connector Types

Currently, Hummingbot supports two CLOB connector standards, each which define how the code encapsulated in a connector folder should offer standardized API endpoints and hook into the Hummingbot client.

* **CLOB Spot**: WebSocket-based connectors to an exchange's spot order book-based markets. Each connector is a folder in the [`hummingbot/connector/exchange`](https://github.com/hummingbot/hummingbot/tree/master/hummingbot/connector/exchange) folder.

* **CLOB Perp**: WebSocket-based connectors to an exchange's perpetual futures order book-based markets. Each connector is a folder in the [`hummingbot/connector/derivative`](https://github.com/hummingbot/hummingbot/tree/master/hummingbot/connector/derivative) folder. By convention, these connector names end in `_perpetual`.

These connector standards allow users to create [Strategies](/strategies) and [Scripts](/scripts) that can operate on different spot and perpetual markets without modification.

### Current CLOB Connectors

Here are the CLOB connectors in the codebase for the current [Epoch](/governance/epochs/). Note that the Foundation prioritizes fixes for connectors from exchanges that are [sponsors or partners](/about/sponsors), so they tend to be more reliable and better maintained.

| Exchange                                | Foundation Partner | Spot | Perp | Connector Guide |
|-----------------------------------------|-------------------|------|------|----------------|
| [Binance](./binance/index.md)           | ✓ | ✓ | ✓ | [Guide](/blog/using-binance-with-hummingbot) |
| [Bitmart](./bitmart/index.md)           | ✓ | ✓ | ✓ |  |
| [Derive](./derive/index.md)             | ✓ | ✓ | ✓ | [Guide](/blog/running-a-trading-bot-with-hummingbot-on-derive/) |
| [dYdX](./dydx/index.md)                 | ✓ | | ✓ | [Guide](/blog/running-a-trading-bot-with-hummingbot-dashboard-on-dydx-v4/) |
| [Gate.io](./gate-io/index.md)           | ✓ | ✓ | ✓ |  |
| [HTX](./huobi/index.md)                 | ✓ | ✓ |  |  |
| [Kucoin](./kucoin/index.md)             | ✓ | ✓ | ✓ |  |
| [OKX](./okx/index.md)                   | ✓ | ✓ | ✓ |  |
| [XRPL](./xrpl.md)                       | ✓ | ✓ |  | [Guide](/blog/-using-xrp-ledger-with-hummingbot/) |
| [AscendEx](./ascendex/index.md)         |  | ✓ |  |  |
| [BingX](./bing_x/index.md)              | | ✓ |  | |
| [Bitstamp](./bitstamp/index.md)         |  | ✓ |  |  |
| [Bitrue](./bitrue.md)                   |  | ✓ |  |  |
| [Bitget](./bitget-perpetual.md)         |  |  | ✓ |  |
| [Bybit](./bybit.md)                     | | ✓ | ✓ |  |
| [BTC Markets](./btc-markets.md)         |  | ✓ |  |  |
| [Coinbase](./coinbase.md)               |  | ✓ |  |  |
| [Cube](./cube/index.md)                 | | ✓ |  |  |
| [Dexalot](./dexalot/index.md)           | | ✓ | ✓ | [Guide](/blog/using-dexalot-with-hummingbot/) |
| [Kraken](./kraken/index.md)             |  | ✓ |  |  |
| [MEXC](./mexc/index.md)                 |  | ✓ |  |  |
| [NDAX](./ndax.md)                       |  | ✓ |  |  |
| [Vertex](./vertex.md)                   | | ✓ |  |  |
| [Foxbit](../exchanges/foxbit/foxbit.md) | | ✓ |  |  |

### Building CLOB Connectors

The Notion templates below summarize the file and functionalities needed to build the latest spot and perpetual connectors standards and support V2 Strategies:

* [Spot Connector v2.1 Notion Template](https://hummingbot-foundation.notion.site/Spot-Connector-v2-1-1cc43830938445c9974f43ef861d59f1): Use this template to build `CLOB spot` connectors that conform 
* [Perp Connector v2.1 Notion Template](https://hummingbot-foundation.notion.site/Perp-Connector-v2-1-57d8391eb54c40929f77067355fd551e): Use this template to build `CLOB perp` connectors that conform 

See [Building Connectors](/developers/connectors) for more information.

If the exchange is not yet supported by Hummingbot, you can submit a governance proposal for it to be included. New connectors may be contributed by community members via [New Connector Proposals](/governance/proposals), which require a pull request with the connector code to the Hummingbot Github repo, along with a minimum HBOT balance to create.
