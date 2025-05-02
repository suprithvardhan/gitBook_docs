# 📬 Subscribe

The `sup_subscribe` method allows clients to subscribe to real-time blockchain events. Instead of requiring clients to poll for updates, this method enables a push-based notification system where the server sends messages to the client when relevant events occur.

## Parameters

- `event_type` (string): Type of event to subscribe to.
  - `new_blocks`: Notifications when new blocks are added to the blockchain.
  - `pending_transactions`: Notifications when new transactions enter the mempool.
  - `logs`: Notifications for specific smart contract events (e.g., ERC-20 transfers).
- `filters` (optional, object): Filters for narrowing events.
  - For `logs`: `address` (string) and `topics` (array) to filter events.
  - For `pending_transactions`: `address` (string) to filter transactions by sender or receiver.

## Returns

- `subscription_id` (string): A unique identifier for managing the subscription.

## Example Request

```json
{
  "jsonrpc": "2.0",
  "method": "sup_subscribe",
  "params": ["new_blocks"],
  "id": 1
}
```

## Example Response

```json
{
  "jsonrpc": "2.0",
  "result": "0x1234abcd5678efgh",
  "id": 1
}
```

## Event Notifications

When an event matching the subscription criteria occurs, the server will push a notification to the client:

```json
{
  "method": "sup_subscription",
  "params": {
    "subscription_id": "0x1234abcd5678efgh",
    "result": {
      "block_hash": "0xabc123...",
      "block_number": 12345,
      "timestamp": 1625097600
    }
  }
}
```

## Example with Filters

### Subscribe to Logs from a Specific Address

```json
{
  "jsonrpc": "2.0",
  "method": "sup_subscribe",
  "params": [
    "logs", 
    {
      "address": "0xContractAddress", 
      "topics": ["0xTransferEvent..."]
    }
  ],
  "id": 1
}
```

### Subscribe to Pending Transactions for a Specific Address

```json
{
  "jsonrpc": "2.0",
  "method": "sup_subscribe",
  "params": [
    "pending_transactions", 
    {
      "address": "0xUserAddress"
    }
  ],
  "id": 1
}
```

## Requirements

- This method requires a WebSocket connection.
- Subscriptions are maintained for the duration of the WebSocket connection.
- If the connection is closed, all subscriptions are automatically removed.

## Error Codes

- `-32000`: Invalid subscription ID
- `-32001`: Unsupported event type
- `-32002`: Subscription limit reached (maximum 10 subscriptions per client)
- `-32003`: Invalid filter parameters

## Notes

- Events are delivered with low latency (typically < 100ms from event detection).
- Excessive subscription usage may be rate-limited to prevent abuse. 