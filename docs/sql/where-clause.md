## The `where` clause

The `where` clause specifies the search condition to be met 
for the documents to be returned, deleted or updated by the query.
There is no limit to the number of predicates that can be included in a search condition.

Used in the [select](select.md), [update](update.md), [delete](delete.md), 
and even sometimes [insert](insert.md) statements.

## Syntax

The `where` clause has one or more predicates:

```
where [condition]
```

```
where [condition1] || [condition2]
```

## Add several conditions

Use logical operators in the `where` clause when you need to add more than one predicate.

You can use logical operators `&&` (and) and `||` (or) to connect predicates:

```
select * [tableName] where [condition1] && [condition2]
```

Use parenthesis to separate predicates logically:

```
select * [tableName] where (([condition1] && [condition2]) || [condition3]) && [condition4]
```

## Construct conditions

Each pridicate included in the search condition in the `where` clause has two parts.
In each part, there can be a reference to the value in a specific field, or a variable,
or a value of any Spheroid Script type, or a complex expression.
Comparing one field value to another field value is allowed.

Spheroid SQL supports the following comparison operators:

- `==` (equal)
- `!=` (not equal)
- `<` (less than)
- `>` (more than)
- `<=` (less than or equal)
- `>=` (more than or equal)

You can also use `in` operator to find documents that are in a list of values.

The power of Spheroid SQL is that it is able not only to compare the
field value to another value, but to perform operations on the field value first, 
and then compare the result to another value, all within the query, 
i.e. on the database side.

## Examples

#### Find documents using comparison operators

The following example updates documents in the "myTable" table in which 
the "currency" field value is not equal to "USD", or 
the "balance" field value is less than or equal to 50:

```
update myTable t
set balance = t.balance + 10, modified = Date()
where t.currency != "USD" || t.balance <= 50
```

The next example get documents in which the "deleted" field has value:

```
select * myTable t where t.deleted != null
```

#### Compare one field value to another field value

The next example gets documents in which the "modified" field value
is equal to the "created" field value:

```
select * from myTable t where t.modified == t.created
```

#### Use a variable inside a condition

The next example returns documents that have the "currency" field value equal to 
"USD":

```
var currencyName = "USD"

select * from myTable t where t.currency == currencyName
```

#### Find documents that are in a list of values

The following example finds documents that are in a list of values using `in` operator:

```
select * transport where t.category in ["car", "bus"]
```

Works the same as the previous example. 
The list of values is assigned to a variable beforehand:

```
var categoryNames = ["car", "bus"]

select * transport where t.category in categoryNames
```

#### Find documents using complex conditions

In the following example, the `t.balance + 10 <= 50` condition will be executed in two steps
for each document: the value in the "balance" field will be incremented by 10 first,
and then the result will be compared to 50:

```
select * from myTable t where t.balance + 10 <= 50
```

## Related Links

- [The insert statement](insert.md)
- [The select statement](select.md)
- [The update statement](update.md)
- [The delete statement](delete.md)
- [Got a question? Submit an issue on GitHub](../submit-an-issue.md)
