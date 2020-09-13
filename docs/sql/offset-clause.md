# The `offset` clause

The `offset` clause allows you to skip a specified number of 
documents to be returned by the query.
It is used as a part of the `select` statement. 

# Syntax

```
offset [offsetNumber]
```

The specified number should be a positive integer.

## Restrictions

In the `select` statement, the `offset` clause is frequently used along with other clauses.
This is the order they should occur in:

- `where` 
- `order by` 
- `limit` 
- `offset`

Any of the clauses above may be omitted.

## Examples

Using a number to set the number of documents to be skipped:

```
select * from myTable offset 5
```

Using a variable to set the number of documents to be skipped:

```
var offsetNumber = 5

select * from myTable offset offsetNumber
```

Using the `offset` clause along with `where`, `order by` and `limit` clauses
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
- [The limit clause](limit-clause.md)
- [Got a question? Submit an issue on GitHub](../submit-an-issue.md)