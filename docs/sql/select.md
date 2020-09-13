# Select

The `select` statement gets a set of documents, or a single document from a table. 
Can also get a value of a single field, or a min, max, average field value in all documents,
or a sum of field values in all documents.

## Syntax

A basic `select` query that gets all documents in a table:

```
select * from [tableName]
```

In each `select` query, the `where` clause can be used to specify the
search condition.

A query that gets all documents in a table that satisfy the search condition:

```
select * from [tableName] where [condition]
```

A query that gets specified fields from all documents in a table:

```
select [fieldName1], [fieldName2] from [tableName] [tableRef]
where [condition]
```

A query that gets the first document from a table:

```
select first() from [tableName] [tableRef]
```

A query that gets specified fields of the first document:

```
select first([fieldName1], [fieldName2]) from [tableName] [tableRef] 
where [condition]
```

A query that gets the value in a single field:

```
select value([fieldName]) from [tableName] [tableRef] where [condition]
```

A query that returns the number of documents in a table
that satisfy the search condition:

```
select count() from [tableName] [tableRef] where [condition]
```

A query that checks if a document satisfying the search condition exists:

```
select exists() from [tableName] [tableRef] where [condition]
```

A query that gets the min value in a specific field:

```
select min([fieldName]) from [tableName] [tableRef] where [condition]
```

A query that gets the max value in a specific field:

```
select max([fieldName]) from [tableName] [tableRef] where [condition]
```

A query that gets the average value in a specific field:

```
select avg([fieldName]) from [tableName] [tableRef] where [condition]
```

A query that gets the sum of values in a specific field:

```
select sum([fieldName]) from [tableName] [tableRef] where [condition]
```

The `offset`, `limit` and `order by` clauses can be used in a `select` query
(see more below).



## Behavior

Spheroid SQL is case-sensitive, so pay attention to the names of tables and fields
you're using in `select` queries.

## Using select with no `where` clause

Use this query to get all documents in a table.
Returns an array of objects each containing all fields it has.

#### Example

The following example selects all documents from the "myTable" table.

```
select * from myTable
```

Result:

```
{
    {
        "id": 1,
        "balance": 10,
        "currency": "USD",
        "type": 1,
        "modified": "2020-07-01T10:32:31.881+00:00"
    },
    {
        "id": 2,
        "balance": 100,
        "currency": "USD",
        "modified": "2020-07-08T15:36:49.330+00:00"
    },
    {
        "id": 3,
        "balance": 200,
        "currency": "USD",
        "modified": "2020-07-31T15:20:40.050+00:00"
    }
}
```

## Using the `where` clause to get a set of documents

If you want to specify the search condition, use the `where` clause.
The query returns an array of objects each containing all fields it has.

Read more about the `where` clause [here](where-clause.md).

#### Example

The following example gets all documents from the "myTable" table 
in which the value in the "currency" field is equal to "USD",
and the value in the "balance" field incremented by 10 is less than or equal to 50.

The "t" variable contains a reference to the table and allows you to distinguish between 
the field name (when used), and the script variable name (when not used).

```
select * from myTable t
where t.currency == "USD" && t.balance + 10 <= 50
```

Result:

```
{
    {
        "id": 1,
        "balance": 10,
        "currency": "USD",
        "type": 1,
        "modified": "2020-07-01T10:32:31.881+00:00"
    }
}
```

## Getting specific fields

Use this kind of query to get not all document fields, but only some of them.

The query returns an array of objects each containing specified fields
(if it has these fields). Each object has an "id" field.

#### Example

In the next example, the query returns an array of objects each having
only the "balance" and the "modified" fields (and the "id" field that was added automatically).

```
select balance, modified from myTable
```

Result:

```
{
    {
        "id": 1,
        "balance": 10,
        "modified": "2020-07-01T10:32:31.881+00:00"
    },
    {
        "id": 2,
        "balance": 100,
        "modified": "2020-07-08T15:36:49.330+00:00"
    },
    {
        "id": 3,
        "balance": 200,
        "modified": "2020-07-31T15:20:40.050+00:00"
    },
}
```

## Getting the first document or its fields

Use the query of this type to get the first document satisfying the search conditions,
or its specific fields only.

Returns an object or null.

#### Example

In the following example, the query only returns an object 
with the "balance" and the "modified" fields (and the "id" field that was added automatically).

The "t" variable contains a reference to the table and allows you to distinguish between 
the field name (when used), and the script variable name (when not used).

```
select first(balance, modified)
from myTable t
where t.currency == "USD" && t.balance + 10 <= 50
```

Result:

```
{
    "id": 1,
    "balance": 10,
    "modified": "2020-07-01T08:32:31.881+00:00"
}
```

## Getting the value of a specific field

Use this kind of query to get the value of a specific field in a document.
Returns the value can be of any Spheroid Script basic type.

#### Example

In the following example, as the document id has not been specified,
the query gets the "balance" field value of a first document that has 
satisfied the search condition.

The "t" variable contains a reference to the table and allows you to distinguish between 
the field name (when used), and the script variable name (when not used).

```
select value(balance)
from myTable t
where t.currency == "USD" && t.balance + 10 <= 50
```

Result: 10.

## Counting documents

Use this kind of query to count the number of documents in a table
satisfying the search conditions.

Returns a number.

#### Example

The next example gets the number of documents in the table where
the "currency" field value is "USD".

The "t" variable contains a reference to the table and allows you to distinguish between 
the field name (when used), and the script variable name (when not used).

```
select count()
from myTable t
where t.currency == "USD"
```

Result: 3.

## Checking if the document exists

Use this query to check if the documents satisfying the search condition exists.

Returns value of type [Boolean](../reference/spheroid/-boolean/index.md).

#### Example

The next example checks if the document exists in the "myTable" table
where the "id" is equal to 3.

The "t" variable contains a reference to the table and allows you to distinguish between 
the field name (when used), and the script variable name (when not used).

```
select exists()
from myTable t
where t.id == 3
```

Result: `true`.

## Getting a min, max, average field value, or a sum of field values

Use the query of this type to get min, max or average value of a specific field,
or a sum of all values in a specific field.

Returns a number.

#### Example

The following example gets the min value in the "balance" field
of a document satisfying the search condition.

The "t" variable contains a reference to the table and allows you to distinguish between 
the field name (when used), and the script variable name (when not used).

```
select min(balance)
from myTable t
where t.currency == "USD" && t.balance + 10 <= 50
```

Result: 10.

## Using the `offset`, `limit` and `order by` clauses

If you want to skip a number of documents to be returned by the query, 
use the `offset` clause (learn more [here](offset-clause.md)).

If you want to restrict the number of documents returned by a query,
use the `limit` clause (learn more [here](limit-clause.md)).

If you want to sort the documents returned by a query, use the `order by` clause
(learn more [here](order-by-clause.md)).

All clauses mentioned above can be used along with each other and with the `where` clause.

## Related Links

- [Spheroid SQL overview](index.md)
- [Hello World app](https://github.com/SpheroidUniverse/SpheroidScript/tree/master/examples/HelloWorld)
- [Got a question? Submit an issue on GitHub](../submit-an-issue.md)