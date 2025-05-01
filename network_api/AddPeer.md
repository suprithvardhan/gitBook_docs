# AddPeer

**Category:** Network  
**Method:** `addPeer`

---

## 🧾 Description

Manually adds a peer to the node's connection list.

---

## 📥 Parameters

| Name      | Type    | Required | Description                               |
|-----------|---------|----------|-------------------------------------------|
| peerAddress | string | Yes     | Libp2p multiaddress of the peer to connect to |
| persistent  | boolean | No     | Keep trying to connect if initial connection fails (default: false) |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "addPeer",
  "params": {
    "peerAddress": "/ip4/192.168.1.101/tcp/8000/p2p/QmZNxLcm4Ks1dBMmHDYsm9KeUSY3TdceuJSqVvRQmDNd9Z",
    "persistent": true
  },
  "id": 1
}
```

## 📤 Returns

Returns information about the connection attempt.

```json
{
  "success": true,
  "peerID": "QmZNxLcm4Ks1dBMmHDYsm9KeUSY3TdceuJSqVvRQmDNd9Z",
  "multiaddress": "/ip4/192.168.1.101/tcp/8000/p2p/QmZNxLcm4Ks1dBMmHDYsm9KeUSY3TdceuJSqVvRQmDNd9Z",
  "connectionStatus": "connected",
  "protocols": [
    "/blockchain/1.0.0",
    "/blockchain/sync/1.0.0"
  ],
  "latency": "45.5ms",
  "direction": "outbound",
  "persistent": true
}
``` 