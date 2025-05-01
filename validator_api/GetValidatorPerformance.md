# GetValidatorPerformance

**Category:** Validator  
**Method:** `getValidatorPerformance`

---

## 🧾 Description

Retrieves performance metrics for a specific validator, including uptime, blocks produced, and rewards earned.

---

## 📥 Parameters

| Name        | Type    | Required | Description                                 |
|-------------|---------|----------|---------------------------------------------|
| validatorId | string  | Yes      | ID of the validator to get performance for  |
| period      | string  | No       | Time period: "day", "week", "month", "all" (default: "day") |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "getValidatorPerformance",
  "params": {
    "validatorId": "0x6b45c8925473f9f5965cd4df2be06a70964bb5a4",
    "period": "week"
  },
  "id": 1
}
```

## 📤 Returns

Returns detailed performance metrics for the specified validator.

```json
{
  "validatorId": "0x6b45c8925473f9f5965cd4df2be06a70964bb5a4",
  "name": "AlphaValidator",
  "period": "week",
  "uptime": 99.8, // percentage
  "blocksProduced": 120,
  "blocksExpected": 122,
  "performance": 98.36, // percentage
  "rewardsEarned": 256.75,
  "averageResponseTime": 52, // milliseconds
  "missedBlocks": 2,
  "slashEvents": 0,
  "delegations": {
    "total": 15,
    "new": 3,
    "withdrawn": 1
  },
  "totalStake": 25000.0,
  "commissionRate": 5.0, // percentage
  "votingPower": 2.5, // percentage of total network
  "ranking": 12, // position among all validators
  "peers": 85,
  "latestBlock": 158025,
  "timeRange": {
    "start": 1628240000,
    "end": 1628845632
  }
}
``` 