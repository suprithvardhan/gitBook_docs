# GetNetworkStats

**Category:** Network  
**Method:** `network_getNetworkStats`

---

## 🧾 Description

Retrieves comprehensive statistics about the network including peer counts, protocols, and blockchain state.

---

## 📥 Parameters

None

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "network_getNetworkStats",
  "params": {},
  "id": 1
}
```

## 📤 Returns

Returns detailed network statistics information.

```json
{
  "nodeID": "QmXGT9A8RmMj7LrEbhf5XM5EsF9Qb3jLRFAuLBYmm1qLeB",
  "listenAddresses": [
    "/ip4/127.0.0.1/tcp/8000",
    "/ip4/192.168.1.100/tcp/8000",
    "/ip4/82.45.67.12/tcp/8000"
  ],
  "connectionCount": 12,
  "bootstrapNodeCount": 3,
  "txnsNodeCount": 4,
  "validatorNodeCount": 5,
  "protocols": [
    "/blockchain/1.0.0",
    "/blockchain/sync/1.0.0",
    "/blockchain/tx/1.0.0",
    "/blockchain/validator/1.0.0"
  ],
  "networkID": "mainnet",
  "chainID": "hybrid-chain-1",
  "bandwidthIn": 1024000,
  "bandwidthOut": 2048000,
  "blockHeight": 1600,
  "lastBlockTime": 1628845632,
  "lastConnectedPeer": "QmVGtMRSvM7pdqbLccJ9FEHJrcQJa2NJX6pgUNxXYkUq7W",
  "lastDisconnectedPeer": "QmNxZRXJgUjx7KXUxWGqCYA5AzjGj8YQqbMwbZKDjBjJqV"
}
``` 