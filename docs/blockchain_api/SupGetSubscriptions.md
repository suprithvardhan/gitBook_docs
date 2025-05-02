# 📋 Get Subscriptions

The `sup_getSubscriptions` method allows clients to retrieve a list of all active subscriptions associated with their current WebSocket connection. This is useful for tracking active subscriptions and managing resources.

## Parameters

This method doesn't require any parameters.

## Returns

- `result` (array of strings): An array containing the subscription IDs of all active subscriptions for the client. Returns an empty array if there are no active subscriptions.

## Example Request

```json
{
  "jsonrpc": "2.0",
  "method": "sup_getSubscriptions",
  "id": 3
}
```

## Example Response

```json
{
  "jsonrpc": "2.0",
  "result": [
    "0x1234abcd5678efgh",
    "0x9876fedc5432abcd"
  ],
  "id": 3
}
```

## Empty Subscriptions Response

```json
{
  "jsonrpc": "2.0",
  "result": [],
  "id": 3
}
```

## Error Handling

If there's a server error, an error response will be returned:

```json
{
  "jsonrpc": "2.0",
  "error": {
    "code": -32603,
    "message": "Internal error"
  },
  "id": 3
}
```

## Error Codes

- `-32603`: Internal server error
- `-32600`: Invalid request

## Notes

- This method only returns subscriptions associated with the current WebSocket connection.
- Each client can have up to 10 active subscriptions by default.
- The order of subscription IDs in the result array is not guaranteed.
- Use this method to audit your application's resource usage and ensure proper subscription management.
- Frequently check unused subscriptions and unsubscribe from them to optimize server resources. 