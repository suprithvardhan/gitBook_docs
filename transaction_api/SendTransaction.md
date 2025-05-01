# SendTransaction

**Category:** Transaction  
**Method:** `sendTransaction`

---

## 🧾 Description

Signs and sends a transaction to the network in a single operation.

---

## 📥 Parameters

| Name      | Type   | Required | Description                                   |
|-----------|--------|----------|-----------------------------------------------|
| from      | string | Yes      | Sender address                                |
| to        | string | Yes      | Recipient address                             |
| amount    | number | Yes      | Amount to send                                |
| privateKey| string | Yes      | Private key of the sender (for signing)       |
| fee       | number | No       | Transaction fee (defaults to minimum fee)     |
| data      | string | No       | Optional data to include with the transaction |
| callback  | string | No       | URL for transaction status callback notifications |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "transaction_sendTransaction",
  "params": {
    "from": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
    "to": "0x3a8e7d92e0c5fca11a9f3c4d072361a1023acdf9",
    "amount": 50.0,
    "privateKey": "9d7086c4b4d445e271d6461a109a9f1f45e034365d0c8089c4e5de7a244a6e4a",
    "fee": 0.001,
    "data": "Transfer payment for services",
    "callback": "https://myapp.com/api/tx-callback"
  },
  "id": 1
}
```

## 📤 Returns

Returns details about the submitted transaction including its ID and initial status.

```json
{
  "txid": "0x7f9b3e6a9a3e5c5b8d8e7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d",
  "from": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
  "to": "0x3a8e7d92e0c5fca11a9f3c4d072361a1023acdf9",
  "amount": 50.0,
  "fee": 0.001,
  "timestamp": 1628762584,
  "status": "pending",
  "confirmations": 0,
  "inMempool": true,
  "callbackRegistered": true,
  "estimatedConfirmationTime": 60 // seconds
}
``` 