# GetNetworkDifficulty

**Category:** Blockchain  
**Method:** `getNetworkDifficulty`

---

## 🧾 Description

Retrieves the current network difficulty and related mining/validation statistics.

---

## 📥 Parameters

None

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "getNetworkDifficulty",
  "params": {},
  "id": 1
}
```

## 📤 Returns

Returns the current network difficulty and related statistics.

```json
{
  "difficulty": 456789,
  "adjustmentFactor": 1.05,
  "targetBlockTime": 30, // seconds
  "actualBlockTime": 28.7, // seconds
  "lastAdjustment": {
    "height": 1500,
    "timestamp": 1628757000,
    "previousDifficulty": 435000,
    "percentChange": 5.01
  },
  "nextAdjustmentEstimate": {
    "height": 1650,
    "estimatedTimestamp": 1628800000,
    "estimatedDifficulty": 479600,
    "percentChange": 5.0
  }
}
``` 