# GetChainInfo

**Category:** Blockchain  
**Method:** `getChainInfo`

---

## 🧾 Description

Retrieves metadata about the blockchain including height, best block hash, and difficulty.

---

## 📥 Parameters

None

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "getChainInfo",
  "params": {},
  "id": 1
}
```

## 📤 Returns

Returns comprehensive information about the current state of the blockchain.

```json
{
  "blocks": 1600,
  "bestBlockHash": "0x9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b",
  "difficulty": 456789,
  "medianTime": 1628845632,
  "chainwork": 7891234567
}
``` 