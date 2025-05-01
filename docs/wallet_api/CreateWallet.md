# CreateWallet

**Category:** Wallet  
**Method:** `createWallet`

---

## 🧾 Description

Creates a new wallet with a randomly generated private/public key pair and address.

---

## 📥 Parameters

None

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "createWallet",
  "params": {},
  "id": 1
}
```

## 📤 Returns

Returns a new wallet with its address, mnemonic phrase, and key data.

```json
{
  "address": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
  "mnemonic": "voice sunny original grass insect knife reject gadget token shoot biology alien",
  "privateKey": "9d7086c4b4d445e271d6461a109a9f1f45e034365d0c8089c4e5de7a244a6e4a",
  "publicKey": "04a8e68d707d71705aec75f1852daa5b2d3694181bd8c2fce3b447e8b0913293b7c0d523730d36518e34c9e2986acf5f98ad18c76cd9d6cbd3cb3f9cac17336330"
}
``` 