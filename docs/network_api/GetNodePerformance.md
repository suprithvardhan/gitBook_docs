# GetNodePerformance

**Category:** Network  
**Method:** `getNodePerformance`

---

## 🧾 Description

Retrieves performance metrics for the current node, including resource usage and operational statistics.

---

## 📥 Parameters

None

---

## 📡 Request

```json
{
  "jsonrpc": "2.0",
  "method": "getNodePerformance",
  "params": {},
  "id": 1
}
```

## 📤 Returns

Returns detailed performance information about the node.

```json
{
  "uptime": 1209600, // seconds (14 days)
  "cpuUsage": 22.5, // percentage
  "memoryUsage": {
    "total": 8192, // MB
    "used": 3584, // MB
    "percentage": 43.75
  },
  "diskUsage": {
    "total": 1024000, // MB
    "used": 512000, // MB
    "percentage": 50,
    "readSpeed": 150, // MB/s
    "writeSpeed": 75 // MB/s
  },
  "networkUsage": {
    "inboundBandwidth": 25.4, // MB/s
    "outboundBandwidth": 18.7, // MB/s
    "connections": 85
  },
  "transactionProcessing": {
    "averageTransactionsPerBlock": 120,
    "transactionsPerSecond": 4.2,
    "pendingTransactions": 250,
    "rejectedTransactions": 15
  },
  "blockProcessing": {
    "averageBlockTime": 30.2, // seconds
    "lastBlockProcessed": 158025,
    "blockValidationTime": 0.85 // seconds
  },
  "peakResourceUsage": {
    "cpuPeak": 78.5,
    "memoryPeak": 6144, // MB
    "connectionsPeak": 120
  }
}
``` 