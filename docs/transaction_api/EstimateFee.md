# EstimateFee

**Category:** Transaction  
**Method:** `estimateFee`

---

## 🧾 Description

Estimates the fee required for a transaction based on current network conditions.

---

## 📥 Parameters

| Name      | Type   | Required | Description                                   |
|-----------|--------|----------|-----------------------------------------------|
| from      | string | Yes      | Sender address                                |
| to        | string | Yes      | Recipient address                             |
| amount    | number | Yes      | Amount to send                                |
| priority  | string | No       | Transaction priority: "low", "medium", "high" (default: "medium") |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "estimateFee",
  "params": {
    "from": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
    "to": "0x3a8e7d92e0c5fca11a9f3c4d072361a1023acdf9",
    "amount": 50.0,
    "priority": "high"
  },
  "id": 1
}
```

## 📤 Returns

Returns estimated fee information.

```json
{
  "fee": 0.002,
  "feeRate": 0.0001,
  "estimatedConfirmationTime": 30,
  "priority": "high",
  "networkCongestion": "low",
  "feeBreakdown": {
    "baseFee": 0.001,
    "priorityFee": 0.001,
    "sizeFee": 0.0
  }
}
``` 