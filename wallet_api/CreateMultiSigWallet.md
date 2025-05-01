# CreateMultiSigWallet

**Category:** Wallet  
**Method:** `createMultiSigWallet`

---

## 🧾 Description

Creates a multi-signature wallet requiring multiple signatures to authorize transactions.

---

## 📥 Parameters

| Name         | Type     | Required | Description                                     |
|--------------|----------|----------|-------------------------------------------------|
| addresses    | string[] | Yes      | List of addresses that can sign transactions    |
| requiredSigs | integer  | Yes      | Number of signatures required for authorization |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "createMultiSigWallet",
  "params": {
    "addresses": [
      "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
      "0x3a8e7d92e0c5fca11a9f3c4d072361a1023acdf9",
      "0x6b45c8925473f9f5965cd4df2be06a70964bb5a4"
    ],
    "requiredSigs": 2
  },
  "id": 1
}
```

## 📤 Returns

Returns information about the created multi-signature wallet.

```json
{
  "address": "0x6742c5fc4d72f1dfc35d8a9e4c3a762bfdd859c0",
  "requiredSigs": 2,
  "totalSigs": 3,
  "participants": [
    "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
    "0x3a8e7d92e0c5fca11a9f3c4d072361a1023acdf9",
    "0x6b45c8925473f9f5965cd4df2be06a70964bb5a4"
  ]
}
``` 