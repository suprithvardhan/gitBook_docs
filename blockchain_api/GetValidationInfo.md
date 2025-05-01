# GetValidationInfo

**Category:** Blockchain  
**Method:** `getValidationInfo`

---

## 🧾 Description

Retrieves detailed validation information for a specific block, including validator signatures and consensus details.

---

## 📥 Parameters

| Name      | Type      | Required | Description                                    |
|-----------|-----------|----------|------------------------------------------------|
| blockHash | string    | No*      | Hash of the block to get validation info for   |
| height    | integer   | No*      | Height of the block to get validation info for |

*Note:* Either blockHash or height must be provided, but not both.

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "getValidationInfo",
  "params": {
    "blockHash": "0x9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b"
  },
  "id": 1
}
```

## 📤 Returns

Returns detailed validation information for the specified block.

```json
{
  "blockHash": "0x9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b",
  "blockHeight": 1580,
  "validatorAddress": "0x6b45c8925473f9f5965cd4df2be06a70964bb5a4",
  "validatorSignature": "0x5e4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d5e4f",
  "consensusRound": 3,
  "validationTimestamp": 1628762584,
  "validationDuration": 250, // milliseconds
  "validators": {
    "total": 15,
    "signed": 12,
    "threshold": 10
  },
  "difficulty": 456789,
  "hashRate": 28500000,
  "isValid": true
}
``` 