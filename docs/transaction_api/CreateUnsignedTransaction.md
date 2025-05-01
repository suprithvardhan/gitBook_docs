# CreateUnsignedTransaction

**Category:** Transaction  
**Method:** `createUnsignedTransaction`

---

## 🧾 Description

Creates an unsigned transaction that can later be signed and submitted to the network.

---

## 📥 Parameters

| Name      | Type   | Required | Description                                   |
|-----------|--------|----------|-----------------------------------------------|
| from      | string | Yes      | Sender address                                |
| to        | string | Yes      | Recipient address                             |
| amount    | number | Yes      | Amount to send                                |
| fee       | number | No       | Transaction fee (defaults to minimum fee)     |
| data      | string | No       | Optional data to include with the transaction |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "transaction_createUnsignedTransaction",
  "params": {
    "from": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
    "to": "0x3a8e7d92e0c5fca11a9f3c4d072361a1023acdf9",
    "amount": 50.0,
    "fee": 0.001,
    "data": "Transfer payment for services"
  },
  "id": 1
}
```

## 📤 Returns

Returns an unsigned transaction object that needs to be signed before broadcasting.

```json
{
  "txid": "0x7f9b3e6a9a3e5c5b8d8e7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d",
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
      "amount": 50.25
    }
  ],
  "outputs": [
    {
      "address": "0x3a8e7d92e0c5fca11a9f3c4d072361a1023acdf9",
      "amount": 50.0
    },
    {
      "address": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
      "amount": 0.249 // Change after fee
    }
  ],
  "status": "unsigned",
  "required": ["signature"]
}
``` 