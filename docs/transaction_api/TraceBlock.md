# TraceBlock

**Category:** Transaction  
**Method:** `traceBlock`

---

## 🧾 Description

Provides detailed traces of all transactions within a specific block, showing complete execution flow.

---

## 📥 Parameters

| Name        | Type    | Required | Description                                |
|-------------|---------|----------|--------------------------------------------|
| blockHash   | string  | No*      | Hash of the block to trace                 |
| blockHeight | integer | No*      | Height of the block to trace               |
| traceType   | string  | No       | Type of trace: "full", "summary", "transfers" (default: "summary") |

*Note:* Either blockHash or blockHeight must be provided, but not both.

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "traceBlock",
  "params": {
    "blockHeight": 1580,
    "traceType": "summary"
  },
  "id": 1
}
```

## 📤 Returns

Returns detailed trace information for all transactions in the block.

```json
{
  "blockHash": "0x9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b",
  "blockHeight": 1580,
  "timestamp": 1628762584,
  "transactionCount": 25,
  "traces": [
    {
      "txid": "0x7f9b3e6a9a3e5c5b8d8e7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d",
      "from": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
      "to": "0x3a8e7d92e0c5fca11a9f3c4d072361a1023acdf9",
      "value": 50.0,
      "gasUsed": 21000,
      "success": true,
      "operations": [
        {
          "type": "transfer",
          "from": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
          "to": "0x3a8e7d92e0c5fca11a9f3c4d072361a1023acdf9",
          "value": 50.0
        }
      ],
      "index": 0,
      "executionTimeMs": 15
    },
    // Additional transaction traces...
  ],
  "gasUsed": 525000,
  "gasLimit": 1000000,
  "stateChanges": 250,
  "executionTimeMs": 375
}
``` 