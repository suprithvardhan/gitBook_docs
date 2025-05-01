# GetBlockchainStats

**Category:** Blockchain  
**Method:** `getBlockchainStats`

---

## 🧾 Description

Retrieves comprehensive statistics about the blockchain's performance, health, and growth.

---

## 📥 Parameters

| Name      | Type    | Required | Description                          |
|-----------|---------|----------|--------------------------------------|
| period    | string  | No       | Time period for statistics: "day", "week", "month", "year", "all" (default: "day") |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "getBlockchainStats",
  "params": {
    "period": "week"
  },
  "id": 1
}
```

## 📤 Returns

Returns detailed blockchain statistics for the specified time period.

```json
{
  "period": "week",
  "blocks": {
    "count": 20160,
    "averageTime": 30.2,
    "averageSize": 8750,
    "averageTransactions": 23.5
  },
  "transactions": {
    "count": 473760,
    "volume": 2850000.5,
    "averageFee": 0.0012,
    "totalFees": 568.51
  },
  "growth": {
    "blockHeight": {
      "start": 1360000,
      "end": 1380160,
      "growth": 20160
    },
    "addresses": {
      "active": 28500,
      "new": 4200
    }
  },
  "network": {
    "hashRate": 28500000,
    "difficulty": 456789,
    "averageDifficulty": 450125,
    "difficultyAdjustments": 2
  },
  "validators": {
    "count": 150,
    "active": 142,
    "newValidators": 5,
    "totalStaked": 3500000.0,
    "averageUptime": 99.7
  },
  "startTime": 1628240000,
  "endTime": 1628845632
}
``` 