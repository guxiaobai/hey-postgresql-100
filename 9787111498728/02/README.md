# 第2章 PostgreSQL 安装与配置

|本期版本|上期版本
|:---:|:---:
`Thu Jul 20 22:01:58 CST 2023` | -


### 2.1.1 在 Debian 或 Ubuntu 下的安装

* 数据目录: `/var/lib/postgresql/<dbversion>/main`


## 2.4 PostgreSQL 的简单配置

> 修改数据目录下的 `postgresql.conf`


### 2.4.1 修改监听的IP和端口

```
listen_addresses = '0.0.0.0'
```