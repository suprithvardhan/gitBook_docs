# GetUTXOs

**Category:** Transaction  
**Method:** `getUTXOs`

---

## 🧾 Description

Retrieves all unspent transaction outputs (UTXOs) for a specific address.

---

## 📥 Parameters

| Name      | Type   | Required | Description                        |
|-----------|--------|----------|------------------------------------|
| address   | string | Yes      | The wallet address to query        |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "transaction_getUTXOs",
  "params": {
    "address": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2"
  },
  "id": 1
}
```

## 📤 Returns

Returns an array of UTXOs associated with the address.

```json
{
  "address": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
  "utxos": [
    {
      "txid": "0x7f9b3e6a9a3e5c5b8d8e7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d",
      "outputIndex": 0,
      "amount": 100.5,
      "blockHeight": 1256,
      "confirmations": 324
    },
    {
      "txid": "0x5a4b3c2d1e0f9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f1a0b9c8d7e6f5a4b",
      "outputIndex": 1,
      "amount": 50.25,
      "blockHeight": 1390,
      "confirmations": 190
    }
  ],
  "total": 150.75,
  "count": 2
}
``` 