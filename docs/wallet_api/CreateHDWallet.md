# CreateHDWallet

**Category:** Wallet  
**Method:** `createHDWallet`

---

## 🧾 Description

Creates a hierarchical deterministic (HD) wallet with multiple derived addresses.

---

## 📥 Parameters

| Name              | Type    | Required | Description                                    |
|-------------------|---------|----------|------------------------------------------------|
| initialAddresses  | integer | No       | Number of initial addresses to generate (default: 1) |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "createHDWallet",
  "params": {
    "initialAddresses": 5
  },
  "id": 1
}
```

## 📤 Returns

Returns an HD wallet with a list of derived addresses.

```json
{
  "mnemonic": "voice sunny original grass insect knife reject gadget token shoot biology alien",
  "addresses": ["0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2", "0x3a8e7d92e0c5fca11a9f3c4d072361a1023acdf9", "..."],
  "count": 5,
  "rootAccount": {
    "address": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
    "privateKey": "9d7086c4b4d445e271d6461a109a9f1f45e034365d0c8089c4e5de7a244a6e4a",
    "publicKey": "04a8e68d707d71705aec75f1852daa5b2d3694181bd8c2fce3b447e8b0913293b7c0d523730d36518e34c9e2986acf5f98ad18c76cd9d6cbd3cb3f9cac17336330"
  }
}
``` 