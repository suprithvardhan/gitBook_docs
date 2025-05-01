# GetStateRoot

**Category:** Blockchain  
**Method:** `getStateRoot`

---

## 🧾 Description

Retrieves the Merkle root hash of the blockchain state at a specific block height.

---

## 📥 Parameters

| Name      | Type    | Required | Description                          |
|-----------|---------|----------|--------------------------------------|
| height    | integer | No       | Block height (default: latest block) |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "getStateRoot",
  "params": {
    "height": 1580
  },
  "id": 1
}
```

## 📤 Returns

Returns the state root hash and related information.

```json
{
  "stateRoot": "0x3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f",
  "blockHash": "0x9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b",
  "blockHeight": 1580,
  "timestamp": 1628762584,
  "stateVersion": 1580,
  "stateSize": 85624789,
  "accounts": 28500,
  "utxos": 124750,
  "stakes": 150
}
``` 