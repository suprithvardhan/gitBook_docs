# GetValidators

**Category:** Validator  
**Method:** `getValidators`

---

## 🧾 Description

Retrieves a list of active validators in the network along with their details.

---

## 📥 Parameters

| Name    | Type   | Required | Description                           |
|---------|--------|----------|---------------------------------------|
| status  | string | No       | Filter by validator status (e.g., "active", "pending", "slashed") |
| limit   | integer| No       | Maximum number of validators to return |
| offset  | integer| No       | Number of validators to skip           |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "getValidators",
  "params": {
    "status": "active",
    "limit": 10,
    "offset": 0
  },
  "id": 1
}
```

## 📤 Returns

Returns a list of validators with their details.

```json
{
  "validators": [
    {
      "address": "0x6b45c8925473f9f5965cd4df2be06a70964bb5a4",
      "publicKey": "0x04a8e68d707d71705aec75f1852daa5b2d3694181bd8c2fce3b447e8b0913293b7c0d523730d36518e34c9e2986acf5f98ad18c76cd9d6cbd3cb3f9cac17336330",
      "status": "active",
      "stake": 5000.0,
      "blocksValidated": 156,
      "uptime": 99.8,
      "score": 9850,
      "lastActive": 1628845632,
      "rewards": 125.75,
      "commission": 5.0
    },
    {
      "address": "0x3a8e7d92e0c5fca11a9f3c4d072361a1023acdf9",
      "publicKey": "0x04b7a2c1d0e9f8a7b6c5d4e3f2a1b0c9d8e7f6a5b4c3d2e1f0a9b8c7d6e5f4a3b2c1d0e9f8a7b6c5d4e3f2a1b0c9d8e7f6a5b4c3d2e1f0a9b8c7d6e5f4a3b2c1d0",
      "status": "active",
      "stake": 7500.0,
      "blocksValidated": 238,
      "uptime": 99.5,
      "score": 9780,
      "lastActive": 1628845600,
      "rewards": 187.25,
      "commission": 4.5
    }
  ],
  "total": 2,
  "activeCount": 2,
  "pendingCount": 0,
  "slashedCount": 0,
  "totalStake": 12500.0
}
``` 