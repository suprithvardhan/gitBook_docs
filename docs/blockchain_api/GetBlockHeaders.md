# GetBlockHeaders

**Category:** Blockchain  
**Method:** `getBlockHeaders`

---

## 🧾 Description

Retrieves headers of multiple blocks within a specified range, optimized for light clients.

---

## 📥 Parameters

| Name         | Type    | Required | Description                          |
|--------------|---------|----------|--------------------------------------|
| startHeight  | integer | Yes      | Starting block height                |
| endHeight    | integer | Yes      | Ending block height                  |
| ascending    | boolean | No       | Sort headers by height (default: true) |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "getBlockHeaders",
  "params": {
    "startHeight": 1500,
    "endHeight": 1510,
    "ascending": true
  },
  "id": 1
}
```

## 📤 Returns

Returns an array of block headers for the specified range.

```json
{
  "headers": [
    {
      "blockNumber": 1500,
      "hash": "0xabc123def456789abcdef0123456789abcdef0123456789abcdef0123456789",
      "previousHash": "0x1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b",
      "timestamp": 1628757000,
      "merkleRoot": "0x2d1e0f9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e",
      "stateRoot": "0x3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f",
      "difficulty": 456000,
      "nonce": 9876543210,
      "transactionCount": 20
    },
    {
      "blockNumber": 1501,
      "hash": "0xdef456789abcdef0123456789abcdef0123456789abcdef0123456789abcdef",
      "previousHash": "0xabc123def456789abcdef0123456789abcdef0123456789abcdef0123456789",
      "timestamp": 1628757300,
      "merkleRoot": "0x3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f",
      "stateRoot": "0x4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d5e4f3a",
      "difficulty": 456100,
      "nonce": 9876543211,
      "transactionCount": 22
    }
    // Additional headers...
  ],
  "count": 11,
  "startHeight": 1500,
  "endHeight": 1510
}
``` 