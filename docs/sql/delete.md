# Delete

The `delete` statement removes one or more documents from a table.
If all documents in a table are removed, a table is also deleted.

## Syntax

A basic `delete` query that deletes all documents in a table:

```
delete [tableName]
```

A `delete` query that will delete one or more documents if a search condition is satisfied:

```
delete [tableName] [tableRef] where [condition]
```

When using the `where` clause, use a special variable 
containing a reference to the table (see examples below).

Read more about the `where` clause [here](where-clause.md).

## Behavior

Spheroid SQL is case-sensitive, so pay attention to the names of tables and fields
you're using in `delete` queries.

## Using delete with no `where` clause

Use this query to delete all documents in a table along with a table itself. 
The query returns an object containing a non-nullable "deleteCount" field:

#### Example

The following example deletes a table:

```
delete myTable
```

Result:

```
{
    "deleteCount": 100
}
```

## Using the `where` clause to delete a set of documents

If you want to specify the search condition to be met 
for the documents to be deleted, use the `where` clause.
You can use variables in a query and make calculations while going through the documents.

The query returns an object containing a non-nullable "deleteCount" field.

Read more about the `where` clause [here](where-clause.md).

#### Example

The following example deletes all documents from the "myTable" table 
in which the value in the "currency" field is equal to "USD",
and the value in the "balance" field incremented by 10 is less than or equal to 50.

The "t" variable contains a reference to the table and allows you to distinguish between 
the field name (when used), and the script variable name (when not used).

```
delete myTable t
where t.currency == "USD" && t.balance + 10 <= 50
```

Result:

```
{
    "deleteCount": 10
}
```

## Using the `where` clause to delete a document by id

If you want to delete one document by id, use the `where` clause and specify the id.

The query returns an object containing a "deleteCount" field.
The value can be 1 or 0. If there is no document with the specified id, value will be 0.

#### Example

The following example deletes one document from the "myTable" table 
in which the "id" equal to 3.

The "t" variable contains a reference to the table and allows you to distinguish between 
the field name (when used), and the script variable name (when not used).

```
delete myTable t where t.id == 3
```

Result:

```
{
    "deleteCount": 1
}
```

## Related Links

- [Spheroid SQL overview](index.md)
- [Hello World app](https://github.com/SpheroidUniverse/SpheroidScript/tree/master/examples/HelloWorld)
- [Got a question? Submit an issue on GitHub](../submit-an-issue.md)