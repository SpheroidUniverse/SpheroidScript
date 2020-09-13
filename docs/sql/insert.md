# Insert

The `insert` statement adds a document to a table or updates an existing document. 
Manages possible duplicates.

## Syntax

A basic `insert` query that adds a new document to the table:

```
insert [tableName] ([field1], [field2]) values ([valueInField1], [valueInField2])
```

An `insert` query that will add a new document only if a duplicate is not found by id:

```
insert [tableName] ([field1], [field2]) values ([valueInField1], [valueInField2])
on duplicate key ignore
```

An `insert` query that will add a new document if a duplicate is not found by id,
and will update specified fields of an existing document otherwise:

```
insert [tableName] [tableRef] ([field1], [field2]) values ([valueInField1], [valueInField2])
on duplicate key update [field2] = [valueInField2]
```

An `insert` query that will add a new document if a duplicate is not found by id,
and will update specified fields of an existing document otherwise 
if a search condition is satisfied:

```
insert [tableName] [tableRef] ([field1], [field2]) values ([valueInField1], [valueInField2])
on duplicate key update [field2] = [valueInField2]
where [condition1]
```

When using the `on duplicate key update` clause
and the `where` clause, use a special variable 
containing a reference to the table (see examples below).

## Behavior

Every document in the database must have an "id" field.
It is of type [UUID](../reference/spheroid/-u-u-i-d/index.md) by default.

The value of any field can be of any Spheroid Script basic type,
including an object with custom fields. This stands for an "id" field as well.

Spheroid SQL is case-sensitive. For example, you can create a document containing
"name" and "Name" fields, this is totally valid.

## Using insert with no id specified

When no id is specified, an
id of type [UUID](../reference/spheroid/-u-u-i-d/index.md) will be created automatically.

Returns an object having an "id" field, and an "insertCount" field. 
The value in the latter can only be 1.

#### Example

The following example adds a new document to the "myTable" table
having three fields: "id" (new UUID value), "balance" (10) and "created" (current date).

```
insert myTable
(balance, created) values (10, Date())
```

Result:

```
{
    "id": UUID("4720b5e3-d72b-441d-a611-63f532259687"),
    "insertCount": 1
}
```

## Using insert with an id specified

When an id is specified but possible duplicate are not handled,
there are two possible outcomes: 

- if the document with the same id doesn't exist, 
the new document will be successfully added,
- if the document with the same id already exists,
the throw exception will be thrown. 

Returns an object having an "id" field, and an "insertCount" field. 
The value in the latter can only be 1.

#### Example

The following example tries to add a new document to the "myTable" table
having three fields: "id" (3), "balance" (10) and "created" (current date).

```
insert myTable
(id, balance, created) values (3, 10, Date())
```

As the document with the same id doesn't exist, the result it:

```
{
    "id": 3,
    "insertCount": 1
}
```

## Using insert with the `on duplicate key ignore` clause 

When you want to add a new document only if a document having the same id doesn't exist,
use the `on duplicate key ignore` clause. It works like this:

- if the document with the same id doesn't exist, 
the new document will be added,
- if the document with the same id already exists,
there will be no changes to the database. 

Returns an object having an "id" field, and an "insertCount" field. 
The value in the latter can be 1 or 0.

#### Example

The following example will add a new document only if a duplicate is not found by id:

```
insert myTable
(id, balance, created) values (3, 10, Date())
on duplicate key ignore
```

As the document with the specified id has been found, 
no changes have been made to the database, and the result is:

```
{
    "id": 3,
    "insertCount": 0
}
```

## Using insert with the `on duplicate key update` clause 

The other way of managing possible duplicates is using the `on duplicate key update` clause.
It works like this:

- if the document with the same id doesn't exist, 
the new document will be added,
- if the document with the same id already exists,
it will be modified. 

Returns an object having an "id" field, an "insertCount" field,
and an "updateCount" field:

- if the new document has been added, the value in the "insertCount" field will be 1,
and the value in the "updateCount" field will be 0,
- if the existing document has been found and modified, 
the value in the "insertCount" field will be 0,
and the value in the "updateCount" field will be 1. Note that the document is only updated
if the new value is different from an old value.

#### Example

The following example will add a new document if a duplicate is not found by id.
Otherwise, it will update an existing document.

The "t" variable contains a reference to the table and allows you to distinguish between 
the field name (when used), and the script variable name (when not used).

```
insert myTable t
(id, balance, created) values (3, 10, Date())
on duplicate key update balance = t.balance + 10, modified = Date()
```

As the document with the specified id has been found, and
it has been modified, and the result is:

```
{
    "id": 3,
    "insertCount": 0,
    "updateCount": 1
}
```

## Using insert with the `on duplicate key update` and `where` clauses 

Sometimes you need to set extra conditions for an update when using 
the `on duplicate key update` clause. Along with the `where` clause it works like this:

- if the document with the same id doesn't exist, 
the new document will be added,
- if the document with the same id already exists,
the condition specified in the `where` clause will be evaluated:
    - if the condition is satisfied, the document will be modified,
    - if the condition isn't satisfied, or the new value is different from an old value, 
    the document will not be modified.

The query returns an object having an "id" field, an "insertCount" field,
and an "updateCount" field:

- if the new document has been added, the value in the "insertCount" field will be 1,
and the value in the "updateCount" field will be 0,
- if the existing document has been found and modified, 
the value in the "insertCount" field will be 0,
and the value in the "updateCount" field will be 1. Note that the document is only updated
if the search condition is satisfied, and the new value is different from an old value.

Read more about the `where` clause [here](where-clause.md).

#### Example

The following example will add a new document if a duplicate is not found by id.
Otherwise, it will update an existing document if the search condition is satisfied.

The "t" variable contains a reference to the table and allows you to distinguish between 
the field name (when used), and the script variable name (when not used).

```
insert myTable t
(id, balance, created) values (3, 10, Date())
on duplicate key update balance = t.balance + 10, modified = Date()
where t.balaince + 10 <= 50
```

As the document with the specified id has been found, and
it has been modified, and the result is:

```
{
    "id": 3,
    "insertCount": 0,
    "updateCount": 1
}
```

## Related Links

- [Spheroid SQL overview](index.md)
- [Hello World app](https://github.com/SpheroidUniverse/SpheroidScript/tree/master/examples/HelloWorld)
- [Got a question? Submit an issue on GitHub](../submit-an-issue.md)