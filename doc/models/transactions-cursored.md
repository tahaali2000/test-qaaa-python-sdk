
# Transactions Cursored

## Structure

`TransactionsCursored`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | [`List[Transaction]`](../../doc/models/transaction.md) | Optional | - |
| `next_cursor` | `str` | Optional | Cursor for the next page of results. |

## Example (as JSON)

```json
{
  "nextCursor": "txn_abc999",
  "data": [
    {
      "id": "id0",
      "amount": 43.32,
      "timestamp": "2016-03-13T12:52:32.123Z"
    },
    {
      "id": "id0",
      "amount": 43.32,
      "timestamp": "2016-03-13T12:52:32.123Z"
    }
  ]
}
```

