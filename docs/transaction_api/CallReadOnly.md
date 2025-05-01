# CallReadOnly

**Category:** Transaction  
**Method:** `callReadOnly`

---

## 🧾 Description

Executes a read-only query against the blockchain state without creating a transaction.

---

## 📥 Parameters

| Name      | Type    | Required | Description                                |
|-----------|---------|----------|--------------------------------------------|
| to        | string  | Yes      | Address to query (typically a contract)    |
| data      | string  | Yes      | Function call data                         |
| caller    | string  | No       | Address to use as the caller (default: zero address) |
| blockHeight | integer | No     | Block height to execute against (default: latest) |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "callReadOnly",
  "params": {
    "to": "0x6b45c8925473f9f5965cd4df2be06a70964bb5a4",
    "data": "0x70a08231000000000000000000000000ef7c8ec4da58e19b7cfd96147dc1f072",
    "caller": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
    "blockHeight": 1580
  },
  "id": 1
}
```

## 📤 Returns

Returns the result of the read-only execution.

```json
{
  "result": "0x000000000000000000000000000000000000000000000000000000000001e240",
  "decodedResult": "123456",
  "gasUsed": 21000,
  "executionTime": 5, // milliseconds
  "blockHeight": 1580,
  "stateRoot": "0x3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f",
  "status": "success"
}
``` 