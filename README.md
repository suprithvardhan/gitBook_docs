# Hybrid Blockchain RPC API Documentation

This documentation provides detailed information about the JSON-RPC API endpoints available in the Hybrid Blockchain network. The API allows developers to interact with the blockchain, manage wallets, create transactions, monitor network status, and more.

## API Categories

The API is organized into the following categories:

### 1. Wallet API
Methods for creating and managing wallets, including:
- Creating new wallets
- Importing existing wallets
- Retrieving wallet information
- Working with hierarchical deterministic (HD) wallets
- Managing multi-signature wallets
- Signing and verifying messages

[View Wallet API Documentation](./wallet_api.md)

### 2. Transaction API
Methods for managing transactions, including:
- Checking balances and UTXOs
- Creating and sending transactions
- Retrieving transaction details
- Monitoring mempool
- Estimating fees

[View Transaction API Documentation](./transaction_api)

### 3. Blockchain API
Methods for querying blockchain data, including:
- Retrieving blocks by hash or height
- Getting blockchain metrics
- Checking network difficulty
- Analyzing circulating supply
- Accessing rich lists

[View Blockchain API Documentation](./blockchain_api)

### 4. Network API
Methods for network interaction, including:
- Getting peer information
- Retrieving network statistics
- Monitoring node status
- Checking sync progress
- Analyzing network performance

[View Network API Documentation](./network_api)

### 5. Validator API
Methods for validator operations, including:
- Registering as a validator
- Monitoring validator status
- Checking uptime and rewards
- Managing stakes

[View Validator API Documentation](./validator_api)

## Using the API

All API requests follow the JSON-RPC 2.0 specification and are sent via HTTP POST to the RPC node's endpoint:

```
http://node-address:port/
```

Each request must include:
- `jsonrpc`: Version of the JSON-RPC protocol ("2.0")
- `method`: The method name to invoke
- `params`: Parameters for the method (object)
- `id`: Request identifier

### Example Request

```json
{
  "jsonrpc": "2.0",
  "method": "wallet_createWallet",
  "params": {},
  "id": 1
}
```

### Example Response

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": {
    "address": "0x8f7492de095ff5c3c7f31a9a9b8291f6340361e2",
    "mnemonic": "voice sunny original grass insect knife reject gadget token shoot biology alien",
    "privateKey": "9d7086c4b4d445e271d6461a109a9f1f45e034365d0c8089c4e5de7a244a6e4a",
    "publicKey": "04a8e68d707d71705aec75f1852daa5b2d3694181bd8c2fce3b447e8b0913293b7c0d523730d36518e34c9e2986acf5f98ad18c76cd9d6cbd3cb3f9cac17336330"
  }
}
```

## Error Handling

When an error occurs, the response will include an error object with a code and message:

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "error": {
    "code": -32600,
    "message": "Invalid Request"
  }
}
```

## Security Considerations

- Never send private keys over unencrypted connections
- Use HTTPS for all production API calls
- Consider using methods that sign transactions locally rather than sending private keys to the node
- For higher security applications, consider using hardware wallets and air-gapped signing

## Rate Limiting

The RPC API implements rate limiting to prevent abuse. Excessive requests may be throttled or blocked.

## Need Help?

If you encounter any issues or have questions about using the API, please visit our [support forum](https://supereum.freeflarum.com/) or [GitHub repository](https://github.com/suprithvm/hybridblockchain). 