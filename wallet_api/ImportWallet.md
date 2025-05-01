# ImportWallet

**Category:** Wallet  
**Method:** `importWallet`

---

## 🧾 Description

Imports an existing wallet using either a mnemonic phrase or a private key.

---

## 📥 Parameters

| Name         | Type   | Required | Description                                       |
|--------------|--------|----------|---------------------------------------------------|
| mnemonic     | string | No*      | Mnemonic phrase used to recover the wallet        |
| privateKey   | string | No*      | Private key in hex format to recover the wallet   |

*Note:* Either mnemonic or privateKey must be provided, but not both.

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "importWallet",
  "params": {
    "mnemonic": "voice sunny original grass insect knife reject gadget token shoot biology alien"
  },
  "id": 1
}
```

## 📤 Returns

Returns the imported wallet's address and key information.

```json
{
  "address": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
  "mnemonic": "voice sunny original grass insect knife reject gadget token shoot biology alien",
  "privateKey": "9d7086c4b4d445e271d6461a109a9f1f45e034365d0c8089c4e5de7a244a6e4a",
  "publicKey": "04a8e68d707d71705aec75f1852daa5b2d3694181bd8c2fce3b447e8b0913293b7c0d523730d36518e34c9e2986acf5f98ad18c76cd9d6cbd3cb3f9cac17336330"
}
``` 