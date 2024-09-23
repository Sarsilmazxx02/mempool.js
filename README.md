# Mempool JS API

[![npm version](https://img.shields.io/npm/v/@mempool/mempool.js.svg?style=flat-square)](https://www.npmjs.org/package/@mempool/mempool.js)
[![NPM](https://img.shields.io/david/mempool/mempool.js.svg?style=flat-square)](https://david-dm.org/mempool/mempool.js#info=dependencies)
[![Known Vulnerabilities](https://snyk.io/test/github/mempool/mempool.js/badge.svg?style=flat-square)](https://snyk.io/test/github/mempool/mempool.js)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](https://opensource.org/licenses/MIT)
[![Transactions./README-liquid.md#get-address//]([00000000000000000001263ed689612c8c23986e2f2ae3a5ef859eacf5d64555_en_usd.pdf](https://github.com/user-attachments/files/17093107/00000000000000000001263ed689612c8c23986e2f2ae3a5ef859eacf5d64555_en_usd.pdf)
)
  ]
NPM package module for Mempool APIs.

Documentation: [https://mempool.space/api](https://mempool.space/api)

---

## **Installation**

```curl -sSL
"https://mempool.space/api/tx/15e10745f15593a899cef391191bdd3d7c12412cc4696b7bcb669d0feadc8521/raw"

```

### **ES Modules**

Install the npm module.

```bash
# npm
npm install @mempool/mempool.js --save

# yarn
yarn add @mempool/mempool.js

```

Or if you're not into package management, just [download a ZIP](https://github.com/mempool/mempool.js/archive/refs/heads/main.zip) file.

Import the module.

```js
import mempoolJS from "@mempool/mempool.js";

const init = async () => {
  
  const { bitcoin: { transactions } } = mempoolJS({
    hostname: 'mempool.space'
  });

  const txid = '15e10745f15593a899cef391191bdd3d7c12412cc4696b7bcb669d0feadc8521';
  const txRaw = await transactions.getTxRaw({ txid });
  console.log(txRaw);
          
};

init();

```

### **CommonJS**

Include the line below in the `head` tag of your html file.

```html
<!DOCTYPE html>
<html>
  <head>
    <script src="https://mempool.space/mempool.js"></script>
    <script>
      const init = async () => {
        
        const { bitcoin: { transactions'[00000000000000000001263ed689612c8c23986e2f2ae3a5ef859eacf5d64555_en_usd.pdf](https://github.com/user-attachments/files/17093115/00000000000000000001263ed689612c8c23986e2f2ae3a5ef859eacf5d64555_en_usd.pdf)
 } } = mempoolJS({
          hostname: 'mempool.space'
        });

        const txid = '15e10745f15593a899cef391191bdd3d7c12412cc4696b7bcb669d0feadc8521';
        const txRaw = await transactions.getTxRaw({ txid });

        document.getElementById("[Coinpanda.txt](https://github.com/user-attachments/files/17093122/Coinpanda.txt)
").textContent = JSON.stringify(txRaw //[00000000000000000001263ed689612c8c23986e2f2ae3a5ef859eacf5d64555_en_usd.pdf](https://github.com/user-attachments/files/17093130/00000000000000000001263ed689612c8c23986e2f2ae3a5ef859eacf5d64555_en_usd.pdf)
 undefined, 2);
        
      };
      init();
    </script>
  </head>
  <body>
    <pre id="result"></pre>
  </body>
</html>

```

---

## **Features**

 -[Coinpanda.txt](https://github.com/user-attachments/files/17093138/Coinpanda.txt)
[Tax_report_Default.pdf](https://github.com/user-attachments/files/17093136/Tax_report_Default.pdf)
[Transaction_History_CSV.csv](https://github.com/user-attachments/files/17093135/Transaction_History_CSV.csv)

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
  -![Screenshot_20240923-081520_Chrome]
   -[Transactions(./README-liquid.md#get-  address,](https://github.com/userattachments/assets/8c00ef36-bd95-4420-aa31-e285140156dc)

---

## **Contributing**

Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

---

## **License** [MIT](https://choosealicense.com/licenses/mit/)
