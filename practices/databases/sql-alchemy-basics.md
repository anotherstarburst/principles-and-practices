---
layout: page
title: SQL Alchemy Basics
---

POPSSS uses SQLAlchemy ORM for use in code. All the models can be found under popsss.model as well as the DBSession which provides an already initialized session to access the Database called DBSession. If you're not familiar with SQLAlchemy, here are some examples of basic use.

### Create

```
from popsss.model import DBSession, MyModel
obj = MyModel()
obj.attr = value
DBSession.add(obj)
```

### Retrieve

```
from popsss.model import DBSession, MyModel

result = DBSession.query(MyModel).filter(MyModel.attr == value).first()
```

### Update

```
from popsss.model import DBSession, MyModel

result = DBSession.query(MyModel).filter(MyModel.attr == value).first()

result.attr = new_value
```

Optional to apply the change immediately: `DBSession.flush()`

### Delete

```
from popsss.model import DBSession, MyModel

DBSession.query(MyModel).filter(MyModel.attr == value).first().delete()
```

Optional to apply the change immediately: `DBSession.flush()`

## Indexes

### Optimise access to data with indexes

If a database query is slow or getting slower as the number of rows is growing in a table, you can often solve this problem by adding an index to the columns used in the where clause of the query.

If the index is over a single column, use `index=True` as a Column argument in the model and then create the respective migration. Otherwise define the index on **table_args** (see the documentation).

For booleans or any value where a column contains a few values that apply to many rows, it will probably make sense to use a [partial index](https://www.postgresql.org/docs/10/indexes-partial.html) when you care only about one of the values in the query, for example True or False.

This is because in general the query optimizer will perform a full-table scan if it cannot create a sensible sub-division of the query space. As a rule of thumb you want to try and identify 10% or less of a table during a query.

**Note**: Indexes make writing to the database slower, so don't add them unless there is a clear need.

### With Foreign Keys

If you're adding a foreign key, please add `index=True` as a Column argument in the model so ensure lookups are fast. Always try to reference an indexed set of columns on the foreign key table.

### Primary Keys

In Postgres [Primary Keys always have an associated index](https://www.postgresql.org/docs/current/sql-createtable.html) and you shouldn't need to specify this.

