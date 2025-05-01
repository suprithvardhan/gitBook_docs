# GetBlockTime

**Category:** Blockchain  
**Method:** `getBlockTime`

---

## 🧾 Description

Retrieves the average block time over recent blocks to assess network performance.

---

## 📥 Parameters

| Name      | Type    | Required | Description                          |
|-----------|---------|----------|--------------------------------------|
| blocks    | integer | No       | Number of blocks to calculate average time (default: 100) |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "getBlockTime",
  "params": {
    "blocks": 200
  },
  "id": 1
}
```

## 📤 Returns

Returns the average block time in seconds.

```json
{
  "averageBlockTime": 30.2,
  "calculatedFromBlocks": 200,
  "targetBlockTime": 30,
  "deviation": 0.67,
  "minBlockTime": 28.1,
  "maxBlockTime": 35.4,
  "startBlock": 1400,
  "endBlock": 1600,
  "timePeriod": 6040 // seconds
}
``` 