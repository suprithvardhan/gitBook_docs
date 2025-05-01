# SignMessage

**Category:** Wallet  
**Method:** `signMessage`

---

## 🧾 Description

Signs a message with the wallet's private key to prove ownership.

---

## 📥 Parameters

| Name     | Type   | Required | Description                         |
|----------|--------|----------|-------------------------------------|
| message  | string | Yes      | Message to sign                     |
| mnemonic | string | Yes      | Mnemonic phrase of the wallet       |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "signMessage",
  "params": {
    "message": "This is a test message to sign",
    "mnemonic": "voice sunny original grass insect knife reject gadget token shoot biology alien"
  },
  "id": 1
}
```

## 📤 Returns

Returns the message, the address that signed it, and the signature.

```json
{
  "address": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
  "message": "This is a test message to sign",
  "signature": "0x7f9b3e6a9a3e5c5b8d8e7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d5a4b3c2d1e0f9a8b7c6d5a4b3c2d1e0f"
}
``` 