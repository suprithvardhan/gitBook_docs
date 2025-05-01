# GetBlockByHash

**Category:** Blockchain  
**Method:** `getBlockByHash`

---

## 🧾 Description

Retrieves detailed information about a specific block identified by its hash.

---

## 📥 Parameters

| Name   | Type   | Required | Description               |
|--------|--------|----------|---------------------------|
| hash   | string | Yes      | The hash of the block     |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "blockchain_getBlockByHash",
  "params": {
    "hash": "0x9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b"
  },
  "id": 1
}
```

## 📤 Returns

Returns comprehensive block data including header, transactions, and validation information.

```json
{
  "header": {
    "blockNumber": 1580,
    "previousHash": "0x1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b",
    "timestamp": 1628762584,
    "merkleRoot": "0x2d1e0f9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e",
    "stateRoot": "0x3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f",
    "difficulty": 456789,
    "nonce": 9876543210,
    "validatorAddress": "0x6b45c8925473f9f5965cd4df2be06a70964bb5a4",
    "validatorProof": "0x4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d5e4f3a",
    "validatorSig": "0x5e4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d5e4f"
  },
  "hash": "0x9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b",
  "size": 8750,
  "transactionCount": 25,
  "transactions": [
    "0x7f9b3e6a9a3e5c5b8d8e7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d",
    "0x1a2b3c4d5e6f7a8b9c0d1e2f3a4b5c6d7e8f9a0b1c2d3e4f5a6b7c8d9e0f1a2b"
    // Additional transaction IDs...
  ],
  "confirmations": 20,
  "cumulativeDifficulty": 7891234567,
  "nextBlockHash": "0x0f9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a",
  "fees": 0.025,
  "rewards": 5.0
}
``` 