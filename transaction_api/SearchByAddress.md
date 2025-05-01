# SearchByAddress

**Category:** Transaction  
**Method:** `searchByAddress`

---

## 🧾 Description

Performs a comprehensive search for all blockchain entities associated with a specific address.

---

## 📥 Parameters

| Name      | Type    | Required | Description                                |
|-----------|---------|----------|--------------------------------------------|
| address   | string  | Yes      | Address to search for                      |
| types     | array   | No       | Entity types to search: ["transactions", "utxos", "validators", "stakes"] (default: all) |
| limit     | integer | No       | Maximum number of results per type (default: 20) |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "searchByAddress",
  "params": {
    "address": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
    "types": ["transactions", "utxos"],
    "limit": 10
  },
  "id": 1
}
```

## 📤 Returns

Returns a comprehensive list of all blockchain entities associated with the address.

```json
{
  "address": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
  "balance": 1250.75,
  "totalAssets": 1750.75,
  "summary": {
    "transactionCount": 128,
    "utxoCount": 7,
    "isValidator": true,
    "stakeAmount": 500.0,
    "firstSeen": 1620000000,
    "lastSeen": 1628845632
  },
  "transactions": [
    {
      "txid": "0x7f9b3e6a9a3e5c5b8d8e7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d",
      "type": "send",
      "amount": 50.0,
      "timestamp": 1628762584,
      "blockHeight": 1580
    }
    // Additional transactions...
  ],
  "utxos": [
    {
      "txid": "0x5a4b3c2d1e0f9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b9c8d7e6f5a4b",
      "outputIndex": 1,
      "amount": 50.25,
      "blockHeight": 1570
    }
    // Additional UTXOs...
  ],
  "hasMore": {
    "transactions": true,
    "utxos": false
  }
}
``` 