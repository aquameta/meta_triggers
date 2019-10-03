# meta_triggers
This extension makes the [meta](https://github.com/aquametalabs/meta) extension writable, by adding insert, update and delete triggers to its views. Typical DDL operations like `create schema foo` can be performed using insert update and delete, e.g. `insert into meta.schema(name) values ('foo')`.

# Install

1. Install the [meta](https://github.com/aquametalabs/meta) extension.  
2. From a shell:
```sh
cd meta_triggers/
make
sudo make install
```
3. From a `pgsql` prompt:
```sql
create extension meta_triggers;
```

# Usage
```
aquameta=# insert into meta.schema(name) values ('my_new_schema');
INSERT 0 1
aquameta=# update meta.schema set name='my_newer_schema' where name='my_new_schema';
UPDATE 1
aquameta=# delete from meta.schema where name='my_newer_schema';
DELETE 1
```
# Documentation

A complete list of supported views is available in the [meta](https://github.com/aquametalabs/meta) extension.
