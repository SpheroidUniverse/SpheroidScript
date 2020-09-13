# The `order by` clause

The `order by` clause controls the sorting of the documents returned by a query. 
It is used as a part of the `select` statement. 

## Syntax

In the `order by` clause you need to specify a field name.

Documents get sorted in the ascending order by default:

```
order by [fieldName]
```

Though you can add `asc` after the field name:

```
order by [fieldName] asc
```

If you want to sort documents in the descending order, add `desc` after the field name:

```
order by [fieldName] desc
```

## Restrictions

In the `select` statement, the `order by` clause is frequently used along with other clauses.
This is the order they should occur in:

- `where` 
- `order by` 
- `limit` 
- `offset`

Any of the clauses above may be omitted.

## Examples

The following example returns all documents from the "myTable" table sorted by
the "created" field in the ascending order:

```
select * from myTable order by created
```

Works the same as the previous example. `asc` is specified explicitly:

```
select * from myTable order by created asc
```

The following example returns all documents from the "myTable" table sorted by
the "created" field in the descending order:

```
select * from myTable order by created desc
```

Using the `order by` clause along with `where`, `limit` and `offset` clauses
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
- [The offset clause](offset-clause.md)
- [The limit clause](limit-clause.md)
- [Got a question? Submit an issue on GitHub](../submit-an-issue.md)