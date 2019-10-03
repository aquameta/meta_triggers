# meta_triggers
This extension makes the [meta](https://github.com/aquametalabs/meta) writable by adding insert, update and delete triggers to its views. Typical DDL operations like `create schema foo` can be performed using only insert update and delete, e.g. `insert into meta.schema(name) values ('foo')`.

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
```sql
insert into meta.schema(name) values ('my_new_schema');
```
