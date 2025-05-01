# GetPendingTransactions

**Category:** Transaction  
**Method:** `getPendingTransactions`

---

## 🧾 Description

Retrieves all pending transactions currently in the mempool, with optional filtering.

---

## 📥 Parameters

| Name      | Type   | Required | Description                                   |
|-----------|--------|----------|-----------------------------------------------|
| address   | string | No       | Filter transactions by address (sender or receiver) |
| limit     | integer| No       | Maximum number of transactions to return      |
| offset    | integer| No       | Number of transactions to skip                |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "transaction_getPendingTransactions",
  "params": {
    "address": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
    "limit": 10,
    "offset": 0
  },
  "id": 1
}
```

## 📤 Returns

Returns a list of pending transactions that haven't been included in a block yet.

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
      "status": "pending",
      "timeInMempool": 125 // seconds
    },
    {
      "txid": "0x1a2b3c4d5e6f7a8b9c0d1e2f3a4b5c6d7e8f9a0b1c2d3e4f5a6b7c8d9e0f1a2b",
      "from": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
      "to": "0x6b45c8925473f9f5965cd4df2be06a70964bb5a4",
      "amount": 25.5,
      "fee": 0.001,
      "timestamp": 1628762600,
      "status": "pending",
      "timeInMempool": 109 // seconds
    }
  ],
  "total": 2,
  "count": 2,
  "mempoolSize": 15
}
``` 