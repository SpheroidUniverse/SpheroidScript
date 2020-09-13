# Spheroid SQL

This guide describes how to start programming in Spheroid SQL.

## About Spheroid SQL

Each app created by a developer in the [Spheroid Demiurge IDE](https://demiurge.spheroiduniverse.io/ide)
has its own isolated database at its disposal.

Spheroid SQL is a query language that ensures communication between 
the developer's app and the database. It combines in itself 
relational databases' simplicity and strictness 
and document-oriented schemaless databases' power and flexibility.

Query syntax is a common problem for a developer working with a database.
Sometimes it's too complex for an unprepared developer; 
sometimes it has too limited capabilities.
Spheroid SQL, on the one hand, has laconic and expressive syntax,
and on the other hand, allows expressing complex logic 
that involves extra calculations on the database side. 

Another common problem for a developer working with a database is the query concurrency.
Without solving this problem, any app is bound to have glitches and breakdowns.
Spheroid SQL has every possibility to ensure app's stable work even when numerous
concurrent queries occur at the same time.

## Syntax instruments

|  Statement | Summary | Featured syntax elements
|---|---|---|
| [Select](select.md) | Gets a set of documents, or a single document from a table. Can also get a single field value, or a min, max, average field value, or a sum of field values. Can count all documents, or check if a document exists. | [where](where-clause.md), [order by](order-by-clause.md), [limit](limit-clause.md), [offset](offset-clause.md)
| [Insert](insert.md) | Adds a document to a table or updates an existing document. Manages possible duplicates. | [where](where-clause.md)
| [Update](update.md) | Changes existing document or a set of documents in a table. | [where](where-clause.md)
| [Delete](delete.md) | Removes one or more document from a table. If all documents in a table are removed, a table is also deleted. | [where](where-clause.md)

For very specific cases, you may need to use the `tableOf()` and the `columnOf()`
functions (read more [here](table-of-column-of-functions.md)).

## Related Links

- [Basic syntax](../basic-syntax.md)
- [Hello World app](https://github.com/SpheroidUniverse/SpheroidScript/tree/master/examples/HelloWorld)
- [Got a question? Submit an issue on GitHub](../submit-an-issue.md)
