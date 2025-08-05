## Authentication

> `/etc/postgresql/16/main/postgresql.conf`

`password_encryption` (`enum`) 



在 [CREATE ROLE](https://www.postgresql.org/docs/16/sql-createrole.html) 或 [ALTER ROLE](https://www.postgresql.org/docs/16/sql-alterrole.html) 中指定密码时，此参数确定用于加密密码的算法。可能的值是 `scram-sha-256`，它将使用 SCRAM-SHA-256 加密密码，以及 `md5`，它将密码存储为 MD5 哈希。默认值为 `scram-sha-256`。



## Client Authentication

> `/etc/postgresql/15/main/pg_hba.conf` 
>
> 客户端身份验证由配置文件控制，该文件传统上名为 `pg_hba.conf`

链接类型(TYPE)|数据库(DATABASE)|用户(USER)|客户机IP地址范围(ADDRESS)|认证方法(METHOD)
---|---|---|---|---
local |all|postgres|-|Peer
local | all|all|-|Peer

---

1️⃣ TYPE

`local`、`host`



2️⃣ DATABASE

* `all`: 与所有数据库匹配



3️⃣ USER

* `all`: 与所有的用户匹配
* `正则表达式`: 以斜杠`/` 开头



4️⃣ ADDRESS

> 起始地址/子网掩码

* `all` 匹配任何IP地址

5️⃣ METHOD

* `peer`:  用当前登录用户名
* `scram-sha-256`









## Ref



* <https://www.postgresql.org/docs/16/runtime-config-connection.html#GUC-PASSWORD-ENCRYPTION>
* <https://www.postgresql.org/docs/16/auth-pg-hba-conf.html>