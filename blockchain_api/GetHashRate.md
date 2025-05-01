# GetHashRate

**Category:** Blockchain  
**Method:** `getHashRate`

---

## 🧾 Description

Retrieves the current estimated hash rate of the blockchain network.

---

## 📥 Parameters

| Name      | Type    | Required | Description                          |
|-----------|---------|----------|--------------------------------------|
| blocks    | integer | No       | Number of blocks to calculate average hash rate (default: 120) |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "getHashRate",
  "params": {
    "blocks": 100
  },
  "id": 1
}
```

## 📤 Returns

Returns the estimated hash rate of the network in hashes per second.

```json
{
  "hashRate": 28500000,
  "hashRateFormatted": "28.5 MH/s",
  "calculatedFromBlocks": 100,
  "timeFrame": 1680, // seconds
  "startHeight": 1500,
  "endHeight": 1600,
  "averageDifficulty": 456789
}
``` 