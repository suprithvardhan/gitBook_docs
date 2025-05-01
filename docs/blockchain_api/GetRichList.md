# GetRichList

**Category:** Blockchain  
**Method:** `getRichList`

---

## 🧾 Description

Retrieves a list of the richest addresses on the blockchain, sorted by balance.

---

## 📥 Parameters

| Name      | Type    | Required | Description                          |
|-----------|---------|----------|--------------------------------------|
| limit     | integer | No       | Maximum number of addresses to return (default: 100) |
| offset    | integer | No       | Number of addresses to skip (default: 0) |
| includeStaked | boolean | No | Include staked tokens in balance calculation (default: true) |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "getRichList",
  "params": {
    "limit": 10,
    "offset": 0,
    "includeStaked": true
  },
  "id": 1
}
```

## 📤 Returns

Returns a list of addresses sorted by balance in descending order.

```json
{
  "addresses": [
    {
      "address": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
      "balance": 1250000.75,
      "staked": 500000.0,
      "total": 1750000.75,
      "percentage": 17.5,
      "transactionCount": 128,
      "lastActive": 1628845632
    },
    {
      "address": "0x3a8e7d92e0c5fca11a9f3c4d072361a1023acdf9",
      "balance": 958750.25,
      "staked": 250000.0,
      "total": 1208750.25,
      "percentage": 12.09,
      "transactionCount": 85,
      "lastActive": 1628842000
    }
    // Additional addresses...
  ],
  "count": 10,
  "total": 10000000.0,
  "circulatingSupply": 10000000.0,
  "concentrationTop10": 68.7 // percentage of supply held by top 10 addresses
}
``` 