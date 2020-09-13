# The `tableOf()` and the `columnOf()` functions

The `tableOf()` and the `columnOf()` functions are 
auxiliary syntax instruments for special occasions.
They allow you to calculate the table name or the field name
on the spot, without knowing it beforehand.

Pass these functions a value of type [String](../reference/spheroid/-string/index.md).
You may want to use them when you 
have the same query for several tables, for instance.

## Example

In the following example you can see a helper function.
When you call this function and pass the table name, the field name and the value to it,
in updates all documents in a specified table, setting the field with the new value.
Note that the value can be of any type.

```
fun setValueToDB(tableName, fieldName, value) {
    update tableOf(tableName) set columnOf(fieldName) = value
}
```

## Related Links

- [The update statement](update.md)
- [Spheroid SQL overview](index.md)
- [Basic syntax](../basic-syntax.md)
- [Got a question? Submit an issue on GitHub](../submit-an-issue.md)