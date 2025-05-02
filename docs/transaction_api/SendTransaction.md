# SendTransaction

**Category:** Transaction  
**Method:** `sendTransaction`

---

## 🧾 Description

Broadcasts a signed transaction to the network.

---

## 📥 Parameters

| Name       | Type   | Required | Description                                   |
|------------|--------|----------|-----------------------------------------------|
| signedTx   | string | Yes      | The signed transaction hex string             |
| maxFeeRate | number | No       | Maximum fee rate to use (in satoshis per byte)|
| callback   | string | No       | URL for transaction status callback notifications |

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "transaction_sendTransaction",
  "params": {
    "signedTx": "0x02f8740184832156008506fc23ac00825208943535353535353535353535353535353535353535880de0b6b3a76400008025a00fe76f2a4b9c5d9d8c958818bd6f6c1a880ff81be2188aa9a40df4c39ef491fa013baf5745fa12a1eb0f2c40625e6c9ec136e052596c71de5d68caad45715d29",
    "maxFeeRate": 50,
    "callback": "https://myapp.com/api/tx-callback"
  },
  "id": 1
}
```

## 📤 Returns

Returns details about the submitted transaction including its ID and initial status.

```json
{
  "txid": "0x7f9b3e6a9a3e5c5b8d8e7a6b5c4d3e2f1a0b9c8d7e6f5a4b3c2d1e0f9a8b7c6d",
  "from": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
  "to": "0x3a8e7d92e0c5fca11a9f3c4d072361a1023acdf9",
  "amount": 50.0,
  "fee": 0.001,
  "timestamp": 1628762584,
  "status": "pending",
  "confirmations": 0,
  "inMempool": true,
  "callbackRegistered": true,
  "estimatedConfirmationTime": 60 // seconds
}
```

## ⚠️ Security Note

Never send your private key in a JSON-RPC request. Instead:
1. Create an unsigned transaction using `createUnsignedTransaction`
2. Sign it locally using your private key with `signTransaction` or wallet software
3. Send only the signed transaction using this method 