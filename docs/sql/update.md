# Update

The `update` statement changes existing document, or a set of documents in a table.
Only modifies a document if the new value is different from an old value.

## Syntax

A basic `update` query that modifies all documents in a table:

```
update [tableName] [tableRef] set [field1] = [valueInField1], [field2] = [valueInField2]
```

An `update` query that will modify one or more documents if a search condition is satisfied:

```
update [tableName] [tableRef] set [field1] = [valueInField1] where [condition]
```

Use a special variable containing a reference to the table (see examples below).

## Behavior

The `update` query can add new fields, or change existing fields values, 
including switching to a different type of any Spheroid Script basic type.
It only modifies a document if the new value is different from an old value.

Spheroid SQL is case-sensitive, so pay attention to the names of tables and fields
you're using in `update` queries.

## Using update with no `where` clause

Use this query to update all documents in a table.
The query returns an object containing a non-nullable "updateCount" field.

#### Example

The next example updates all documents in the "myTable" table.
It sets the "modified" field value to the current date,
and increments the "balance" field value by 10.

This example shows how Spheroid SQL solves the concurrency problem
by getting the current field value and modifying it withing the query. 

The "t" variable contains a reference to the table and allows you to distinguish between 
the field name (when used), and the script variable name (when not used).

```
update myTable t
set balance = t.balance + 10, modified = Date()
```

Result:

```
{
    "updateCount": 100
}
```

## Using the `where` clause to update a set of documents

If you want to specify the search condition to be met 
for the documents to be updated, use the `where` clause.
You can use variables in a query and make calculations while going through the documents.

The query returns an object containing a non-nullable "updateCount" field.

Read more about the `where` clause [here](where-clause.md).

#### Example

The next example updates all documents in the "myTable" table where
in which the value in the "currency" field is equal to "USD",
and the value in the "balance" field incremented by 10 is less than or equal to 50.

It sets the "modified" field value to the current date,
and increments the "balance" field value by 10.

The "t" variable contains a reference to the table and allows you to distinguish between 
the field name (when used), and the script variable name (when not used).

```
update myTable t
set balance = t.balance + 10, modified = Date()
where t.currency == "USD" && t.balance + 10 <= 50
```

Result:

```
{
    "updateCount": 10
}
```

## Using the `where` clause to update a document by id

If you want to update one document by id, use the `where` clause and specify the id.

The query returns an object containing a non-nullable "updateCount" field.

#### Example

The following example updates one document from the "myTable" table 
in which the "id" equal to 3.

It sets the "modified" field value to the current date,
and increments the "balance" field value by 10.

The "t" variable contains a reference to the table and allows you to distinguish between 
the field name (when used), and the script variable name (when not used).

```
update myTable t
set balance = t.balance + 10, modified = Date() where t.id == 3

```

Result:

```
{
    "updateCount": 1
}
```

## Related Links

- [Spheroid SQL overview](index.md)
- [Hello World app](https://github.com/SpheroidUniverse/SpheroidScript/tree/master/examples/HelloWorld)
- [Got a question? Submit an issue on GitHub](../submit-an-issue.md)