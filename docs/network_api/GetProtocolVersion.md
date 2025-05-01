# GetProtocolVersion

**Category:** Network  
**Method:** `getProtocolVersion`

---

## 🧾 Description

Retrieves the protocol version and compatibility information for the node.

---

## 📥 Parameters

None

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "getProtocolVersion",
  "params": {},
  "id": 1
}
```

## 📤 Returns

Returns detailed protocol version information.

```json
{
  "protocolVersion": "1.0.0",
  "minCompatibleVersion": "0.9.0",
  "maxCompatibleVersion": "1.1.0",
  "networkID": "mainnet",
  "chainID": "hybrid-chain-1",
  "supportedProtocols": [
    {
      "name": "/blockchain",
      "version": "1.0.0"
    },
    {
      "name": "/blockchain/sync",
      "version": "1.0.0"
    },
    {
      "name": "/blockchain/tx",
      "version": "1.0.0"
    },
    {
      "name": "/blockchain/validator",
      "version": "1.0.0"
    }
  ],
  "implementationVersion": "1.0.5",
  "clientVersion": "Hybrid Blockchain Go implementation v1.0.5"
}
``` 