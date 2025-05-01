# ExportState

**Category:** Blockchain  
**Method:** `exportState`

---

## 🧾 Description

Exports the blockchain state at a specific block height, useful for backup or analysis.

---

## 📥 Parameters

| Name      | Type    | Required | Description                          |
|-----------|---------|----------|--------------------------------------|
| height    | integer | No       | Block height (default: latest block) |
| format    | string  | No       | Export format: "json", "protobuf", "cbor" (default: "json") |
| components | array   | No       | Specific state components to export: ["utxos", "accounts", "validators", "all"] (default: "all") |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "exportState",
  "params": {
    "height": 1580,
    "format": "json",
    "components": ["utxos", "validators"]
  },
  "id": 1
}
```

## 📤 Returns

Returns a base64-encoded string of the exported state data.

```json
{
  "height": 1580,
  "blockHash": "0x9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b",
  "stateRoot": "0x3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f",
  "timestamp": 1628762584,
  "format": "json",
  "components": ["utxos", "validators"],
  "size": 45678,
  "data": "eyJoZWlnaHQiOjE1ODAsInN0YXRlIjp7InV0eG9zIjpbeyJ0eGlkIjoiMHg3ZjliM2U2YTlhM2U1YzViOGQ...truncated for brevity",
  "checksum": "0x5a4b3c2d1e0f9a8b7c6d5e4f3a2b1c0d"
}
``` 