# DebugTransaction

**Category:** Transaction  
**Method:** `debugTransaction`

---

## 🧾 Description

Provides detailed debug information about a transaction's execution, especially useful for failed transactions.

---

## 📥 Parameters

| Name      | Type    | Required | Description                              |
|-----------|---------|----------|------------------------------------------|
| txid      | string  | Yes      | Transaction ID to debug                  |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "debugTransaction",
  "params": {
    "txid": "0x7f9b3e6a9a3e5c5b8d8e7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d"
  },
  "id": 1
}
```

## 📤 Returns

Returns detailed debug information about the transaction.

```json
{
  "txid": "0x7f9b3e6a9a3e5c5b8d8e7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d",
  "status": "confirmed",
  "blockHeight": 1580,
  "execution": {
    "steps": [
      {
        "operation": "verify_signature",
        "success": true,
        "details": "Valid ECDSA signature for public key 0x04a8e68d707d71705aec75f1852daa5..."
      },
      {
        "operation": "check_funds",
        "success": true,
        "details": "Sufficient funds in UTXO pool: 50.25 >= 50.001"
      },
      {
        "operation": "execute_transfer",
        "success": true,
        "details": "Transferred 50.0 to 0x3a8e7d92e0c5fca11a9f3c4d072361a1023acdf9"
      },
      {
        "operation": "create_change",
        "success": true,
        "details": "Created change output of 0.249 to 0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2"
      },
      {
        "operation": "apply_fee",
        "success": true,
        "details": "Applied fee of 0.001"
      }
    ],
    "gasUsed": 21000,
    "gasLimit": 21000,
    "gasPrice": 0.0000000476,
    "executionTime": 15, // milliseconds
    "logs": [
      "Transaction verification started at 2023-08-15T14:25:10Z",
      "UTXO selection complete - 1 inputs selected",
      "Transaction validation successful",
      "Transaction included in block 1580"
    ]
  },
  "verifiedBy": ["validator1", "validator2", "validator3"],
  "replayProtection": "enforced"
}
```