# GetStateProof

**Category:** Blockchain  
**Method:** `getStateProof`

---

## 🧾 Description

Generates a Merkle proof for a specific address or transaction in the state tree, which can be used to verify inclusion in the blockchain.

---

## 📥 Parameters

| Name      | Type    | Required | Description                          |
|-----------|---------|----------|--------------------------------------|
| address   | string  | No*      | Address to generate proof for        |
| txid      | string  | No*      | Transaction ID to generate proof for |
| height    | integer | No       | Block height (default: latest block) |

*Note:* Either address or txid must be provided, but not both.

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "getStateProof",
  "params": {
    "address": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
    "height": 1580
  },
  "id": 1
}
```

## 📤 Returns

Returns a cryptographic proof of inclusion in the state tree.

```json
{
  "address": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
  "blockHeight": 1580,
  "blockHash": "0x9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b",
  "stateRoot": "0x3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f",
  "timestamp": 1628762584,
  "proof": [
    "0x7f9b3e6a9a3e5c5b8d8e7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d",
    "0x1a2b3c4d5e6f7a8b9c0d1e2f3a4b5c6d7e8f9a0b1c2d3e4f5a6b7c8d9e0f1a2b",
    "0x2d1e0f9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e"
  ],
  "value": {
    "balance": 1250.75,
    "nonce": 15,
    "data": "0x4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d5e4f3a"
  },
  "isValid": true
}
``` 