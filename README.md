# deepstreamHub data-dump loader for PostgreSQL

A tool to load data into PostgreSQL from [deepstreamHub data dumps](https://dashboard.deepstreamhub.com/export).
The `./load` tool reads an exported, unzipped json file and uses it to populate
a PostgreSQL table that can be consumed by the
[deepstream.io PostgreSQL storage connector](https://github.com/deepstreamIO/deepstream.io-storage-postgres).

The `schema` option corresponds to the `schema` option on the storage adaptor.

The connector will connect to the database using credentials in the
`PGHOST`, `PGPORT`, `PGDATABASE`, `PGUSER` and `PGPASSWORD` environment variables.

```
  Usage: ./load [options] <file ...>


  Options:

    -s, --schema <schema>  schema name to store the data under (default 'ds')
    -h, --help             output usage information
```
