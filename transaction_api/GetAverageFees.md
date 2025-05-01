# GetAverageFees

**Category:** Transaction  
**Method:** `getAverageFees`

---

## 🧾 Description

Retrieves information about average transaction fees over recent time periods.

---

## 📥 Parameters

| Name      | Type    | Required | Description                                |
|-----------|---------|----------|--------------------------------------------|
| period    | string  | No       | Time period: "hour", "day", "week", "month" (default: "hour") |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "getAverageFees",
  "params": {
    "period": "day"
  },
  "id": 1
}
```

## 📤 Returns

Returns detailed fee statistics for the specified period.

```json
{
  "period": "day",
  "averageFee": 0.00115,
  "medianFee": 0.001,
  "minFee": 0.0001,
  "maxFee": 0.0025,
  "feeRate": {
    "fastest": 0.0025,
    "fast": 0.0015,
    "average": 0.001,
    "slow": 0.0005
  },
  "estimatedConfirmationTime": {
    "fastest": "10 seconds",
    "fast": "30 seconds",
    "average": "1 minute",
    "slow": "5 minutes"
  },
  "transactionCount": 34680,
  "feeDistribution": [
    {
      "range": "0.0001-0.0005",
      "count": 5202,
      "percentage": 15
    },
    {
      "range": "0.0005-0.001",
      "count": 13872,
      "percentage": 40
    },
    {
      "range": "0.001-0.0015",
      "count": 10404,
      "percentage": 30
    },
    {
      "range": "0.0015-0.002",
      "count": 3468,
      "percentage": 10
    },
    {
      "range": "0.002+",
      "count": 1734,
      "percentage": 5
    }
  ],
  "timeStart": 1628676000,
  "timeEnd": 1628762400
}
``` 