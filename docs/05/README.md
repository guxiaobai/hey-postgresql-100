# 05 createuser

|本期版本|上期版本
|:---:|:---:
`Sat Aug  2 11:26:27 CST 2025` | -


```bash
$ createuser  ${app_name} -P
```
* `-P`：提示输入密码

---
* createuser 创建一个新的 PostgreSQL 用户（或者更准确地说，是一个角色）
* createuser 是 SQL 命令 CREATE ROLE 的包装器。通过此实用程序创建用户和通过其他访问服务器的方法创建用户之间没有有效区别。

## Ref



* <https://www.postgresql.org/docs/16/app-createuser.html>

