# GetSyncStatus

**Category:** Network  
**Method:** `getSyncStatus`

---

## 🧾 Description

Retrieves detailed information about the blockchain synchronization status of the node.

---

## 📥 Parameters

None

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "getSyncStatus",
  "params": {},
  "id": 1
}
```

## 📤 Returns

Returns comprehensive information about the sync status of the node.

```json
{
  "syncing": true,
  "currentBlockHeight": 1200,
  "peersCount": 12,
  "peersConnected": [
    "QmZNxLcm4Ks1dBMmHDYsm9KeUSY3TdceuJSqVvRQmDNd9Z",
    "QmVGtMRSvM7pdqbLccJ9FEHJrcQJa2NJX6pgUNxXYkUq7W"
  ],
  "syncComplete": false,
  "networkID": "mainnet",
  "chainID": "hybrid-chain-1",
  "targetBlockHeight": 1600,
  "remainingBlocks": 400,
  "syncSpeed": 15.8,
  "estimatedTimeRemaining": 1520,
  "syncStartTime": 1628840000
}
``` 