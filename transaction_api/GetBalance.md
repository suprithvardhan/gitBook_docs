# GetBalance

**Category:** Transaction  
**Method:** `getBalance`

---

## 🧾 Description

Retrieves the balance of a specified address from the UTXO pool.

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
  "method": "transaction_getBalance",
  "params": {
    "address": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2"
  },
  "id": 1
}
```

## 📤 Returns

Returns the current balance of the address.

```json
{
  "address": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
  "balance": 1250.75,
  "confirmed": 1250.75,
  "unconfirmed": 0.0
}
``` 