# GetPeerInfo

**Category:** Network  
**Method:** `getPeerInfo`

---

## 🧾 Description

Retrieves detailed information about all connected peers on the network.

---

## 📥 Parameters

None

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "network_getPeerInfo",
  "params": {},
  "id": 1
}
```

## 📤 Returns

Returns an array of peer information objects with connection details and node types.

```json
[
  {
    "id": "QmZNxLcm4Ks1dBMmHDYsm9KeUSY3TdceuJSqVvRQmDNd9Z",
    "addresses": [
      "/ip4/192.168.1.101/tcp/8000",
      "/ip4/120.65.45.32/tcp/8000"
    ],
    "protocols": [
      "/blockchain/1.0.0",
      "/blockchain/sync/1.0.0",
      "/blockchain/tx/1.0.0"
    ],
    "isBootstrap": true,
    "isTXNS": false,
    "connectedSince": "2023-08-15T14:25:10Z",
    "latency": "45.5ms"
  },
  {
    "id": "QmVGtMRSvM7pdqbLccJ9FEHJrcQJa2NJX6pgUNxXYkUq7W",
    "addresses": [
      "/ip4/192.168.1.102/tcp/8000",
      "/ip4/135.75.23.12/tcp/8000"
    ],
    "protocols": [
      "/blockchain/1.0.0",
      "/blockchain/sync/1.0.0",
      "/blockchain/tx/1.0.0",
      "/blockchain/validator/1.0.0"
    ],
    "isBootstrap": false,
    "isTXNS": true,
    "connectedSince": "2023-08-15T15:05:32Z",
    "latency": "78.2ms"
  }
]
``` 