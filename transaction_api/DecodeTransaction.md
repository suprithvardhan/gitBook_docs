# DecodeTransaction

**Category:** Transaction  
**Method:** `decodeTransaction`

---

## 🧾 Description

Decodes a raw transaction hex string into a human-readable format.

---

## 📥 Parameters

| Name      | Type    | Required | Description                                |
|-----------|---------|----------|--------------------------------------------|
| hexString | string  | Yes      | Hex-encoded transaction data to decode     |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "decodeTransaction",
  "params": {
    "hexString": "0x7f9b3e6a9a3e5c5b8d8e7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d5a4b3c2d1e0f9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f"
  },
  "id": 1
}
```

## 📤 Returns

Returns the decoded transaction data in a structured format.

```json
{
  "txid": "0x7f9b3e6a9a3e5c5b8d8e7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d",
  "version": 1,
  "locktime": 0,
  "from": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
  "to": "0x3a8e7d92e0c5fca11a9f3c4d072361a1023acdf9",
  "amount": 50.0,
  "fee": 0.001,
  "data": "Transfer payment for services",
  "timestamp": 1628762584,
  "inputs": [
    {
      "txid": "0x5a4b3c2d1e0f9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b9c8d7e6f5a4b",
      "outputIndex": 1,
      "amount": 50.25,
      "scriptSig": "0x4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d5e4f3a"
    }
  ],
  "outputs": [
    {
      "address": "0x3a8e7d92e0c5fca11a9f3c4d072361a1023acdf9",
      "amount": 50.0,
      "scriptPubKey": "0x1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b"
    },
    {
      "address": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
      "amount": 0.249, // Change after fee
      "scriptPubKey": "0x2b1c0d9e8f7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d5e4f3a2b1c"
    }
  ],
  "isFullySigned": true,
  "signatureType": "ECDSA",
  "publicKey": "0x04a8e68d707d71705aec75f1852daa5b2d3694181bd8c2fce3b447e8b0913293b7c0d523730d36518e34c9e2986acf5f98ad18c76cd9d6cbd3cb3f9cac17336330"
}
``` 