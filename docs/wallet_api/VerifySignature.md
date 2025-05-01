# VerifySignature

**Category:** Wallet  
**Method:** `verifySignature`

---

## 🧾 Description

Verifies if a signature was created by the owner of a specific address.

---

## 📥 Parameters

| Name      | Type   | Required | Description                              |
|-----------|--------|----------|------------------------------------------|
| address   | string | Yes      | Address of the signer                    |
| message   | string | Yes      | Original message that was signed         |
| signature | string | Yes      | Signature to verify                      |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "verifySignature",
  "params": {
    "address": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
    "message": "This is a test message to sign",
    "signature": "0x7f9b3e6a9a3e5c5b8d8e7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d5a4b3c2d1e0f9a8b7c6d5a4b3c2d1e0f"
  },
  "id": 1
}
```

## 📤 Returns

Returns the verification result.

```json
{
  "address": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
  "message": "This is a test message to sign",
  "isValid": true
}
``` 