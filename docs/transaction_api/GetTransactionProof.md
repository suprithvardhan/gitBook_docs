# GetTransactionProof

**Category:** Transaction  
**Method:** `getTransactionProof`

---

## 🧾 Description

Generates a Merkle proof for a transaction to verify its inclusion in a block.

---

## 📥 Parameters

| Name      | Type    | Required | Description                                |
|-----------|---------|----------|--------------------------------------------|
| txid      | string  | Yes      | Transaction ID to generate proof for       |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "getTransactionProof",
  "params": {
    "txid": "0x7f9b3e6a9a3e5c5b8d8e7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d"
  },
  "id": 1
}
```

## 📤 Returns

Returns a Merkle proof for the transaction.

```json
{
  "txid": "0x7f9b3e6a9a3e5c5b8d8e7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d",
  "blockHeight": 1580,
  "blockHash": "0x9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b",
  "merkleRoot": "0x2d1e0f9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e",
  "timestamp": 1628762584,
  "transactionIndex": 5,
  "siblings": [
    "0xa8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c",
    "0xb9c8d7e6f5a4b3c2d1e0f9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b9c8d",
    "0xc0d9e8f7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d5e4f3a2b1c0d9e"
  ],
  "path": "left,right,left",
  "isValid": true
}
``` 