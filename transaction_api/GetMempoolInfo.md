# GetMempoolInfo

**Category:** Transaction  
**Method:** `getMempoolInfo`

---

## 🧾 Description

Retrieves current information about the transaction mempool.

---

## 📥 Parameters

None

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "getMempoolInfo",
  "params": {},
  "id": 1
}
```

## 📤 Returns

Returns detailed information about the current state of the mempool.

```json
{
  "size": 15,
  "bytes": 12750,
  "maxMempool": 300000000, // 300 MB
  "mempoolMinFee": 0.00001,
  "totalFees": 0.015,
  "avgFee": 0.001,
  "avgTransactionSize": 850,
  "oldestTime": 1628761500,
  "newestTime": 1628762600,
  "transactionsByFee": {
    "high": 3,
    "medium": 8,
    "low": 4
  },
  "clearRate": 25, // transactions per block
  "estimatedWaitTime": {
    "high": "10 seconds",
    "medium": "30 seconds",
    "low": "2 minutes"
  }
}
``` 