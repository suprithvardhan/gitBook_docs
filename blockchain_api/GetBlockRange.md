# GetBlockRange

**Category:** Blockchain  
**Method:** `getBlockRange`

---

## 🧾 Description

Retrieves a range of blocks from the blockchain within specified starting and ending heights.

---

## 📥 Parameters

| Name      | Type    | Required | Description                          |
|-----------|---------|----------|--------------------------------------|
| startHeight | integer | Yes      | Starting block height               |
| endHeight   | integer | Yes      | Ending block height                 |
| includeTransactions | boolean | No | Include transaction details (default: false) |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "getBlockRange",
  "params": {
    "startHeight": 1500,
    "endHeight": 1505,
    "includeTransactions": false
  },
  "id": 1
}
```

## 📤 Returns

Returns an array of blocks within the specified range.

```json
{
  "blocks": [
    {
      "header": {
        "blockNumber": 1500,
        "previousHash": "0x1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b",
        "timestamp": 1628757000,
        "merkleRoot": "0x2d1e0f9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e",
        "difficulty": 456000
      },
      "hash": "0xabc123def456789abcdef0123456789abcdef0123456789abcdef0123456789",
      "size": 8500,
      "transactionCount": 20
    },
    {
      "header": {
        "blockNumber": 1501,
        "previousHash": "0xabc123def456789abcdef0123456789abcdef0123456789abcdef0123456789",
        "timestamp": 1628757300,
        "merkleRoot": "0x3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f",
        "difficulty": 456100
      },
      "hash": "0xdef456789abcdef0123456789abcdef0123456789abcdef0123456789abcdef",
      "size": 8520,
      "transactionCount": 22
    }
    // Additional blocks in the range...
  ],
  "count": 6,
  "startHeight": 1500,
  "endHeight": 1505
}
``` 