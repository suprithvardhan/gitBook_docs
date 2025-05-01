# StakeTokens

**Category:** Validator  
**Method:** `stakeTokens`

---

## 🧾 Description

Stakes tokens to become a validator or increase an existing validator's stake.

---

## 📥 Parameters

| Name      | Type   | Required | Description                                     |
|-----------|--------|----------|-------------------------------------------------|
| address   | string | Yes      | Address of the validator                        |
| amount    | number | Yes      | Amount of tokens to stake                       |
| privateKey| string | Yes      | Private key to sign the staking transaction     |
| publicKey | string | Yes      | Public key to use for validation                |
| commission| number | No       | Commission percentage (between 0-100)           |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "stakeTokens",
  "params": {
    "address": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
    "amount": 5000.0,
    "privateKey": "9d7086c4b4d445e271d6461a109a9f1f45e034365d0c8089c4e5de7a244a6e4a",
    "publicKey": "04a8e68d707d71705aec75f1852daa5b2d3694181bd8c2fce3b447e8b0913293b7c0d523730d36518e34c9e2986acf5f98ad18c76cd9d6cbd3cb3f9cac17336330",
    "commission": 5.0
  },
  "id": 1
}
```

## 📤 Returns

Returns information about the staking transaction and validator status.

```json
{
  "txid": "0x7f9b3e6a9a3e5c5b8d8e7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d",
  "address": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
  "status": "pending",
  "amount": 5000.0,
  "totalStake": 5000.0,
  "activationHeight": 1650,
  "commission": 5.0,
  "estimatedActivationTime": 1628850000
}
``` 