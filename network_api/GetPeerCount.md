# GetPeerCount

**Category:** Network  
**Method:** `getPeerCount`

---

## 🧾 Description

Retrieves the current count of connected peers to the node.

---

## 📥 Parameters

| Name    | Type    | Required | Description                                      |
|---------|---------|----------|--------------------------------------------------|
| details | boolean | No       | Include detailed peer type counts (default: false) |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "getPeerCount",
  "params": {
    "details": true
  },
  "id": 1
}
```

## 📤 Returns

Returns the count of connected peers with optional detailed breakdown.

```json
{
  "total": 85,
  "inbound": 32,
  "outbound": 53,
  "types": {
    "validators": 18,
    "fullNodes": 42,
    "lightNodes": 25
  },
  "bootstrapped": 78,
  "ipv4": 53,
  "ipv6": 32,
  "countries": {
    "US": 22,
    "DE": 15,
    "JP": 10,
    "SG": 8,
    "other": 30
  },
  "averageUptime": 86400, // seconds
  "maxConnections": 150
}
``` 