# ValidateAddress

**Category:** Blockchain  
**Method:** `validateAddress`

---

## 🧾 Description

Validates an address format and returns information about the address type and validity.

---

## 📥 Parameters

| Name      | Type    | Required | Description                          |
|-----------|---------|----------|--------------------------------------|
| address   | string  | Yes      | Address to validate                  |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "validateAddress",
  "params": {
    "address": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2"
  },
  "id": 1
}
```

## 📤 Returns

Returns validation information for the provided address.

```json
{
  "address": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
  "isValid": true,
  "type": "standard",
  "checksumMatch": true,
  "metadata": {
    "isContract": false,
    "isMultiSig": false,
    "isValidator": true,
    "hasBalance": true
  }
}
``` 