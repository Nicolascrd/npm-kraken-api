# Node Kraken

NodeJS Client Library for the Kraken (kraken.com) API

This is an asynchronous node client for the kraken.com API. It exposes all the API methods found here: https://www.kraken.com/help/api through the `publicMethod` and `privateMethod` methods.

### Installation

```bash
npm install Nicolascrd/npm-kraken-api
```

### Example Usage:

```typescript
const key = "..."; // API Key
const secret = "..."; // API Private Key
import { KrakenClient } from "kraken-api";
const kraken = new KrakenClient(key, secret);

(async () => {
  // Display user's balance
  console.log(await kraken.api("Balance"));

  // Get Ticker Info
  console.log(await kraken.api("Ticker", { pair: "XXBTZUSD" }));
})();
```
### Credit:

Forked from https://github.com/nothingisdead/npm-kraken-api 