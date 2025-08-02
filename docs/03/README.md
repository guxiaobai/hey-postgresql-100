# 03 The PostgreSQL User Account

|本期版本|上期版本
|:---:|:---:
`Sat Aug  2 11:21:35 CST 2025` | -

> Pre-packaged versions of PostgreSQL will typically create a suitable user account automatically during package installation.

> **PostgreSQL 的预打包版本在安装过程中通常会自动创建一个合适的用户账户**

```bash
# 查看系统中是否有 postgres 用户
$ id postgres

# 以 postgres 用户身份进入 PostgreSQL 控制台
$ sudo -u postgres psql
```


## Ref

* <https://www.postgresql.org/docs/16/postgres-user.html>