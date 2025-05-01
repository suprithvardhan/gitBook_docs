# GetRecentTransactions

**Category:** Transaction  
**Method:** `getRecentTransactions`

---

## 🧾 Description

Retrieves a list of the most recent transactions from the blockchain.

---

## 📥 Parameters

| Name      | Type    | Required | Description                                |
|-----------|---------|----------|--------------------------------------------|
| limit     | integer | No       | Maximum number of transactions to return (default: 20) |
| offset    | integer | No       | Number of transactions to skip (default: 0) |
| includeMempool | boolean | No  | Include pending transactions from mempool (default: true) |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "getRecentTransactions",
  "params": {
    "limit": 10,
    "offset": 0,
    "includeMempool": true
  },
  "id": 1
}
```

## 📤 Returns

Returns a list of recent transactions across the blockchain.

```json
{
  "transactions": [
    {
      "txid": "0x7f9b3e6a9a3e5c5b8d8e7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d",
      "from": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
      "to": "0x3a8e7d92e0c5fca11a9f3c4d072361a1023acdf9",
      "amount": 50.0,
      "fee": 0.001,
      "timestamp": 1628762584,
      "blockHeight": 1580,
      "status": "confirmed"
    },
    {
      "txid": "0x1a2b3c4d5e6f7a8b9c0d1e2f3a4b5c6d7e8f9a0b1c2d3e4f5a6b7c8d9e0f1a2b",
      "from": "0x3a8e7d92e0c5fca11a9f3c4d072361a1023acdf9",
      "to": "0x6b45c8925473f9f5965cd4df2be06a70964bb5a4",
      "amount": 25.5,
      "fee": 0.001,
      "timestamp": 1628762600,
      "status": "pending",
      "inMempool": true
    }
    // Additional transactions...
  ],
  "count": 10,
  "newestTime": 1628762600,
  "oldestTime": 1628760000,
  "timeRange": 2600 // seconds
}
``` 