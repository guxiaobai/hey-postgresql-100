# 06 createdb

|本期版本|上期版本
|:---:|:---:
`Sat Aug  2 11:49:10 CST 2025` | -

```bash
createdb -O ${app_name} ${app_name}_production -E UTF8 -e
```

* `-O` ${app_name}：指定数据库的所有者（Owner）
* `${app_name}_production`：数据库名称，通常是应用名加上 _production 后缀，用于生产环境。
* `-E UTF8`：指定数据库编码为 UTF-8。
* `-e`：回显实际执行的 SQL 语句（有助于调试）

## Ref

* <https://www.postgresql.org/docs/16/app-createdb.html>