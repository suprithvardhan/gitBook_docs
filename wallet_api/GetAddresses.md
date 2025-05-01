# GetAddresses

**Category:** Wallet  
**Method:** `getAddresses`

---

## 🧾 Description

Retrieves a list of addresses from an HD wallet with their corresponding balances.

---

## 📥 Parameters

| Name     | Type    | Required | Description                             |
|----------|---------|----------|-----------------------------------------|
| mnemonic | string  | Yes      | Mnemonic phrase of the HD wallet        |
| start    | integer | No       | Starting index for addresses (default: 0) |
| count    | integer | No       | Number of addresses to return (default: 10) |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "getAddresses",
  "params": {
    "mnemonic": "voice sunny original grass insect knife reject gadget token shoot biology alien",
    "start": 0,
    "count": 5
  },
  "id": 1
}
```

## 📤 Returns

Returns a list of addresses from the HD wallet with their balances.

```json
{
  "addresses": [
    {
      "index": 0,
      "address": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
      "balance": 1250.75
    },
    {
      "index": 1,
      "address": "0x3a8e7d92e0c5fca11a9f3c4d072361a1023acdf9",
      "balance": 50.0
    }
  ],
  "total": 2,
  "start": 0,
  "end": 1
}
``` 