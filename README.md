# Node Kraken

NodeJS Client Library for the Kraken (kraken.com) API

This is an asynchronous node client for the kraken.com API. It exposes all the API methods found here: https://www.kraken.com/help/api through the `publicMethod` and `privateMethod` methods.

### Installation

```bash
npm install Nicolascrd/npm-kraken-api
```

### Example Usage Private Method:

```typescript
const key = "..."; // API Key
const secret = "..."; // API Private Key
import { KrakenClient } from "ts-kraken-api";
const kraken = new KrakenClient(key, secret);

(async () => {
  // Display user's balance
  const options = {}
  const callback = () => undefined;
  console.log(await kraken.privateMethod("Balance", options, callback));
})();
```

### Example Usage Public Method:

```typescript
import { KrakenClient } from "ts-kraken-api";
const kraken = new KrakenClient("", "");

(async () => {
  // Get Ticker Info
  const options = {pair: "XXBTZUSD"}
  const callback = () => undefined
  console.log(await kraken.api("Ticker", options, callback));
})
```
### Credit:

Forked from https://github.com/nothingisdead/npm-kraken-api
