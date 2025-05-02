# 🚫 Unsubscribe

The `sup_unsubscribe` method allows clients to terminate an active subscription to blockchain events. This method is essential for resource management, allowing clients to stop receiving notifications when they are no longer needed.

## Parameters

- `subscription_id` (string): The unique identifier of the subscription to terminate, as returned by the `sup_subscribe` method.

## Returns

- `result` (boolean): `true` if the subscription was successfully terminated, `false` if the subscription ID was not found or the unsubscribe operation failed.

## Example Request

```json
{
  "jsonrpc": "2.0",
  "method": "sup_unsubscribe",
  "params": ["0x1234abcd5678efgh"],
  "id": 2
}
```

## Example Response

```json
{
  "jsonrpc": "2.0",
  "result": true,
  "id": 2
}
```

## Error Handling

If the subscription ID doesn't exist or cannot be terminated, the result will be `false`:

```json
{
  "jsonrpc": "2.0",
  "result": false,
  "id": 2
}
```

If an invalid parameter is provided or there's a server error, an error response will be returned:

```json
{
  "jsonrpc": "2.0",
  "error": {
    "code": -32000,
    "message": "Invalid subscription ID"
  },
  "id": 2
}
```

## Error Codes

- `-32000`: Invalid subscription ID format
- `-32602`: Invalid parameters (e.g., missing subscription ID)

## Notes

- Subscriptions are automatically terminated when the WebSocket connection is closed.
- Clients should unsubscribe from events they no longer need to monitor to reduce server load and network traffic.
- There is no limit to how many subscriptions can be terminated in a session.
- After unsubscribing, the client will no longer receive notifications for the specified subscription ID. 