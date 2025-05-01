# GetNodeStatus

**Category:** Network  
**Method:** `getNodeStatus`

---

## 🧾 Description

Retrieves comprehensive status information about the current node including sync status, chain height, and roles.

---

## 📥 Parameters

None

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "getNodeStatus",
  "params": {},
  "id": 1
}
```

## 📤 Returns

Returns detailed status information about the node.

```json
{
  "nodeID": "QmXGT9A8RmMj7LrEbhf5XM5EsF9Qb3jLRFAuLBYmm1qLeB",
  "version": "1.0.0",
  "uptime": 1628845632,
  "blockHeight": 1600,
  "lastBlockTime": 1628845600,
  "peerCount": 12,
  "syncing": false,
  "mining": false,
  "validating": true,
  "networkID": "mainnet",
  "chainID": "hybrid-chain-1",
  "peerIDCount": 12,
  "bootstrapConnected": true,
  "syncComplete": true
}
``` 