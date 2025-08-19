
!!! note
    This connector is being migrated to the new Gateway architecture. Currently available in Gateway Legacy (v2.2) only. See [Gateway Installation](/gateway/installation) for setup instructions.

## 🛠 Connector Info

- **Exchange Type**: Decentralized Exchange (DEX)
- **Market Type**: Automatic Market Maker (AMM)


| Component                                        | Status    | Notes |
| ------------------------------------------------ | --------- | ----- |
| [2️⃣ AMM Connector](#2-amm-connector)             | ✅        |
| [3️⃣ Range AMM Connector](#3-range-amm-connector) | Not built |
| [🔀 Spot Connector](#spot-connector)             | Not built |
| [🕯 AMM Data Feed](#amm-data-feed)                | Not built |

## ℹ️ Exchange Info

- **Website**: <https://carbondefi.xyz>
- **CoinMarketCap**: <https://coinmarketcap.com/exchanges/carbon/>
- **CoinGecko**: <https://www.coingecko.com/en/exchanges/carbon>
- **Fees**: <https://docs.carbondefi.xyz/carbon/introducing-carbon/fees-and-payments>

## 🔑 How to Connect

Create a wallet on one of the supported networks below:

| Chain      | Networks  |
| ---------- | --------- |
| `ethereum` | `mainnet` |

From inside the Hummingbot client, run `gateway connect carbonamm` in order to connect your wallet:

```
Which chain do you want carbonamm to connect to? (ethereum) >>>
Which network do you want carbonamm to connect to? (mainnet) >>>
Enter your ethereum-mainnet private key >>>>
```

If connection is successful (ethereum-mainnet):

```
The carbonamm connector now uses wallet [pubKey] on ethereum-mainnet
```

## 2️⃣ AMM Connector

_Integration to this DEX's swap pricing and execution endpoints_

- **ID**: `carbonamm`
- **Connection Type**: REST via [Gateway](/gateway)
- **API Docs**: <https://docs.carbondefi.xyz/developer-guides/carbon-sdk>
- **Folder**: <https://github.com/hummingbot/gateway/tree/main/src/connectors/carbon>
- **Default Configs**: <https://github.com/hummingbot/gateway/blob/main/src/templates/carbon.yml>

### Endpoints

- `/amm/price`
- `/amm/trade`
- `/amm/estimateGas`

For more info, run Gateway and go to https:localhost:8080 in your browser to see detailed documentation for each endpoint.
