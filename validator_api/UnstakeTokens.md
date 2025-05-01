# UnstakeTokens

**Category:** Validator  
**Method:** `unstakeTokens`

---

## 🧾 Description

Removes staked tokens from a validator, returning them to the wallet balance after an unbonding period.

---

## 📥 Parameters

| Name         | Type     | Required | Description                                  |
|--------------|----------|----------|----------------------------------------------|
| validatorId  | string   | Yes      | ID of the validator to unstake from          |
| amount       | number   | Yes      | Amount of tokens to unstake                  |
| address      | string   | Yes      | Address to receive the unstaked tokens       |
| privateKey   | string   | No       | Private key to sign the unstaking request (if not using wallet authentication) |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "unstakeTokens",
  "params": {
    "validatorId": "0x6b45c8925473f9f5965cd4df2be06a70964bb5a4",
    "amount": 500.0,
    "address": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2"
  },
  "id": 1
}
```

## 📤 Returns

Returns information about the unstaking operation.

```json
{
  "transactionId": "0x7f9b3e6a9a3e5c5b8d8e7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d",
  "validatorId": "0x6b45c8925473f9f5965cd4df2be06a70964bb5a4",
  "address": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
  "amount": 500.0,
  "unbondingPeriod": 259200, // 3 days in seconds
  "completionTime": 1629022000, // Unix timestamp
  "status": "pending",
  "remainingStake": 1500.0,
  "fee": 0.001
}
``` 