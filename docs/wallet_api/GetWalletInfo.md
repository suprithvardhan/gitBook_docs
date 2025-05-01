# GetWalletInfo

**Category:** Wallet  
**Method:** `getWalletInfo`

---

## 🧾 Description

Retrieves wallet information including balance, transaction count, and validator status.

---

## 📥 Parameters

| Name      | Type   | Required | Description                              |
|-----------|--------|----------|------------------------------------------|
| address   | string | Yes      | Wallet address to retrieve info for      |
| mnemonic  | string | No       | Optional mnemonic to include public key  |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "getWalletInfo",
  "params": {
    "address": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2"
  },
  "id": 1
}
```

## 📤 Returns

Returns detailed information about the wallet.

```json
{
  "address": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
  "balance": 1250.75,
  "nonce": 5,
  "utxoCount": 7,
  "transactions": 12,
  "isValidator": false
}
``` 