## 没有权限创建数据库


|本期版本|上期版本
|:---:|:---:
`Tue Aug 25 20:23:55 CST 2026` | -

```bash
root@vm63:~/tihuoka# bin/rails db:create
PG::InsufficientPrivilege: ERROR:  permission denied to create database
Couldn't create 'tihuoka_development' database. Please check your configuration.
bin/rails aborted!
ActiveRecord::StatementInvalid: PG::InsufficientPrivilege: ERROR:  permission denied to create database (ActiveRecord::StatementInvalid)


Caused by:
PG::InsufficientPrivilege: ERROR:  permission denied to create database (PG::InsufficientPrivilege)

Tasks: TOP => db:create
(See full trace by running task with --trace)
```

## 命令行工具

```bash
createuser -d 
```

## SQL语句

```bash
CREATE ROLE
```

## Ansible

```yml
role_attr_flags: "CREATEDB"
```

## Ref

- <https://www.postgresql.org/docs/16/app-createuser.html>
- <https://www.postgresql.org/docs/16/sql-createrole.html>
- <https://docs.ansible.com/projects/ansible/latest/collections/community/postgresql/postgresql_user_module.html#ansible-collections-community-postgresql-postgresql-user-module>