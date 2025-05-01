# GetCirculatingSupply

**Category:** Blockchain  
**Method:** `getCirculatingSupply`

---

## 🧾 Description

Retrieves the current circulating supply of tokens in the blockchain network.

---

## 📥 Parameters

None

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "getCirculatingSupply",
  "params": {},
  "id": 1
}
```

## 📤 Returns

Returns detailed information about the token supply statistics.

```json
{
  "circulatingSupply": 10000000.0,
  "totalSupply": 21000000.0,
  "percentCirculating": 47.62,
  "stakedSupply": 3500000.0,
  "percentStaked": 35.0,
  "burnedTokens": 50000.0,
  "rewardsMinted": 2550000.0,
  "lastUpdated": 1628845632
}
``` 