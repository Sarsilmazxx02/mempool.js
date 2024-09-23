# Mempool JS API

[![npm version](https://img.shields.io/npm/v/@mempool/mempool.js.svg?style=flat-square)](https://www.npmjs.org/package/@mempool/mempool.js)
[![NPM](https://img.shields.io/david/mempool/mempool.js.svg?style=flat-square)](https://david-dm.org/mempool/mempool.js#info=dependencies)
[![Known Vulnerabilities](https://snyk.io/test/github/mempool/mempool.js/badge.svg?style=flat-square)](https://snyk.io/test/github/mempool/mempool.js)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](https://opensource.org/licenses/MIT)

# NPM package module for Mempool APIs.

Documentation: [https://mempool.space/api](https://mempool.space/api)

---

## **Installation**

```
{
  "latest": {
    "id": 163,
    "added": "2022-08-30T00:00:00.000Z",
    "channel_count": 81690,
    "node_count": 15851,
    "total_capacity": 460820222344,
    "tor_nodes": 11455,
    "clearnet_nodes": 2305,
    "unannounced_nodes": 974,
    "avg_capacity": 5641085,
    "avg_fee_rate": 497,
    "avg_base_fee_mtokens": 915,
    "med_capacity": 1500000,
    "med_fee_rate": 40,
    "med_base_fee_mtokens": 100,
    "clearnet_tor_nodes": 1117
  }
}

```
### **ES Modules**

Install the npm module.

```bash
# npm
$ npm install @mempool/mempool.js --save

# yarn
$ yarn add @mempool/mempool.js
```

Or if you're not into package management, just [download a ZIP](https://github.com/mempool/mempool.js/archive/refs/heads/main.zip) file.

Import the module.

```js
import mempoolJS from '@mempool/mempool.js';

// default mempool.space endpointsconst { bitcoin, liquid } = mempoolJS();

// (optional) your custom endpoints
const { bitcoin } = mempoolJS({
  protocol: 'https', // optional, defaults to http for localhost, otherwise https
  hostname: 'mempool.space',
  network: 'testnet' // 'signet' | 'testnet' | 'mainnet',
  config: { // optional axios request config to add to requests
    headers: {
      authorization: 'Basic auth'
    }
  }
});

// Liquid API
const { liquid } = mempoolJS({
  protocol: 'https', // optional, defaults to http for localhost, otherwise https
  hostname: 'liquid.network',
  network: 'liquid' // 'liquid' | 'liquidtestnet'
});

```
  ### ** Düğüm İstatistiklerini Al **

  Belirtilen . node'a ait detayları döndürür :pubKey.

```j.son
curl -sSL "https://mempool.space/api/v1/lightning/nodes/033ac2f9f7ff643c235cc247c521663924aff73b26b38118a6c6821460afcde1b3"

{
  "public_key": "033ac2f9f7ff643c235cc247c521663924aff73b26b38118a6c6821460afcde1b3",
  "alias": "Red.de.Rayos",
  "first_seen": 1521504055,
  "updated_at": 1661869523,
  "color": "#68f442",
  "sockets": "84.44.203.181:9735",
  "as_number": 8422,
  "city_id": 2886242,
  "country_id": 2921044,
  "subdivision_id": 2861876,
  "longitude": 6.9489,
  "latitude": 50.9298,
  "iso_code": "DE",
  "as_organization": "NetCologne GmbH",
  "city": {
    "de": "Köln",
    "en": "Cologne",
    "es": "Colonia",
    "fr": "Cologne",
    "ja": "ケルン",
    "pt-BR": "Colônia",
    "ru": "Кёльн",
    "zh-CN": "科隆"
  },
  "country": {
    "de": "Deutschland",
    "en": "Germany",
    "es": "Alemania",
    "fr": "Allemagne",
    "ja": "ドイツ連邦共和国",
    "pt-BR": "Alemanha",
    "ru": "Германия",
    "zh-CN": "德国"
  },
  "subdivision": {
    "de": "Nordrhein-Westfalen",
    "en": "North Rhine-Westphalia",
    "es": "Renania del Norte-Westfalia",
    "fr": "Rhénanie du Nord-Westphalie",
    "ru": "Северный Рейн-Вестфалия"
  },
  "active_channel_count": 55,
  "capacity": "31505027",
  "opened_channel_count": 55,
  "closed_channel_count": 111
}

```

### **CommonJS**

Include the line below in the `head` tag of your html file.

```html
<script type="text/javascript" src="https://mempool.space/mempool.js"></script>
```

Call `mempoolJS()` function to access the API methods.

```js
// default mempool.space endpoints
const { bitcoin } = mempoolJS();

// (optional) your custom endpoints
const { bitcoin } = mempoolJS({
  protocol: 'https', // optional, defaults to http for localhost, otherwise https
  hostname: 'mempool.space',
  network: 'testnet', // 'signet' | 'testnet' | 'mainnet'
});

// Liquid API
const { liquid } = mempoolJS({
  protocol: 'https', // optional, defaults to http for localhost, otherwise https
  hostname: 'liquid.network',
  network: 'liquid' // 'liquid' | 'liquidtestnet'
});
```

---

## **Features**

- [Bitcoin](./README-bitcoin.md)
  - [Addresses](./README-bitcoin.md#get-address)
  - [Blocks](./README-bitcoin.md#get-blocks)
  - [Difficulty Adjustment](./README-bitcoin.md#get-difficulty-adjustment)
  - [Fees](./README-bitcoin.md#get-fees)
  - [Lightning](./README-bitcoin.md#get-network-stats)
  - [Mempool](./README-bitcoin.md#get-mempool)
  - [Transactions](./README-bitcoin.md#get-transactions)
  - [Websocket](./README-bitcoin.md#init-websocket)
- [Liquid](./README-liquid.md#get-address)
  - [Addresses](./README-liquid.md#get-address)
  - [Assets](./README-liquid.md#get-address)
  - [Blocks](./README-liquid.md#get-address)
  - [Fees](./README-liquid.md#get-address)
  - [Mempool](./README-liquid.md#get-address)
  - [Transactions](./README-liquid.md#get-address)
  - [Websocket](./README-liquid.md#init-websocket)

---

## **Contributing**

Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

---

## **License** [MIT](https://choosealicense.com/licenses/mit/)
