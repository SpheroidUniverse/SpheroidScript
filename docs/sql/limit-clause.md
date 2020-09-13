# The `limit` clause

The `limit` clause restricts the number of documents returned by a query. 
It is used as a part of the `select` statement. 

## Syntax

```
limit [limitCount]
```

The specified number should be a positive integer.

## Restrictions

In the `select` statement, the `limit` clause is frequently used along with other clauses.
This is the order they should occur in:

- `where` 
- `order by` 
- `limit` 
- `offset`

Any of the clauses above may be omitted.

## Examples

Using a number to set the number of documents to be returned:

```
select * from myTable limit 10
```

Using a variable to set the number of documents to be returned:

```
var limitCount = 10

select * from myTable limit limitCount
```

Using the `limit` clause along with `where`, `order by` and `offset` clauses
in the `select` statement:

```
select * from myTable t
where t.currency == "USD" 
order by id
limit 10 
offset 5
```

## Related Links

- [The select statement](select.md)
- [The where clause](where-clause.md)
- [The order by clause](order-by-clause.md)
- [The offset clause](offset-clause.md)
- [Got a question? Submit an issue on GitHub](../submit-an-issue.md)
