# Transaction

```python
transaction_controller = client.transaction
```

## Class Name

`TransactionController`

## Methods

* [Fetch With Offset](../../doc/controllers/transaction.md#fetch-with-offset)
* [Fetch With Cursor](../../doc/controllers/transaction.md#fetch-with-cursor)
* [Fetch With Link](../../doc/controllers/transaction.md#fetch-with-link)


# Fetch With Offset

Fetch transactions using Offset-based Pagination

```python
def fetch_with_offset(self,
                     offset=0,
                     limit=10)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `offset` | `int` | Query, Optional | The number of records to skip before selecting transactions.<br><br>**Default**: `0`<br><br>**Constraints**: `>= 0` |
| `limit` | `int` | Query, Optional | Number of transactions per page.<br><br>**Default**: `10`<br><br>**Constraints**: `>= 1`, `<= 100` |

## Response Type

[`TransactionsOffset`](../../doc/models/transactions-offset.md)

## Example Usage

```python
offset = 0

limit = 10

result = transaction_controller.fetch_with_offset(
    offset=offset,
    limit=limit
)
```


# Fetch With Cursor

Fetch transactions using Cursor-based Pagination

```python
def fetch_with_cursor(self,
                     cursor=None,
                     limit=10)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cursor` | `str` | Query, Optional | The unique identifier (cursor) to fetch the next set of results. |
| `limit` | `int` | Query, Optional | Number of transactions per page.<br><br>**Default**: `10`<br><br>**Constraints**: `>= 1`, `<= 100` |

## Response Type

[`TransactionsCursored`](../../doc/models/transactions-cursored.md)

## Example Usage

```python
cursor = 'txn_abc123'

limit = 10

result = transaction_controller.fetch_with_cursor(
    cursor=cursor,
    limit=limit
)
```


# Fetch With Link

Fetch transactions using Link-based Pagination

```python
def fetch_with_link(self,
                   page=1,
                   size=10)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `page` | `int` | Query, Optional | The page number to fetch.<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1` |
| `size` | `int` | Query, Optional | Number of transactions per page.<br><br>**Default**: `10`<br><br>**Constraints**: `>= 1`, `<= 100` |

## Response Type

[`TransactionsLinked`](../../doc/models/transactions-linked.md)

## Example Usage

```python
page = 1

size = 10

result = transaction_controller.fetch_with_link(
    page=page,
    size=size
)
```

