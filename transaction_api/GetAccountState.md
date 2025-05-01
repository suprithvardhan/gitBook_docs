# GetAccountState

**Category:** Transaction  
**Method:** `getAccountState`

---

## 🧾 Description

Retrieves comprehensive account state information including balance, transaction count, and validator status.

---

## 📥 Parameters

| Name      | Type   | Required | Description                        |
|-----------|--------|----------|------------------------------------|
| address   | string | Yes      | The wallet address to query        |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "transaction_getAccountState",
  "params": {
    "address": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2"
  },
  "id": 1
}
```

## 📤 Returns

Returns detailed account state information for the specified address.

```json
{
  "address": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
  "balance": 1250.75,
  "nonce": 15,
  "utxoCount": 7,
  "transactionCount": 28,
  "isValidator": true,
  "lastActiveHeight": 1580,
  "firstActiveHeight": 1200,
  "stakes": 2000.0,
  "status": "active"
}
``` 