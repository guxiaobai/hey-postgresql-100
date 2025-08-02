# 04 Creating a Database Cluster

|本期版本|上期版本
|:---:|:---:
`Sat Aug  2 11:23:24 CST 2025` | -


**在你开始做任何事情之前，必须在磁盘上初始化一个数据库存储区域我们称其为“数据库集群（database cluster）”**

👉 这一步通常通过 initdb 命令完成，用于创建数据库所需的文件结构。

```bash
# brew info postgresql@16
initdb --locale=C -E UTF-8 /opt/homebrew/var/postgresql@16
```

---

**初始化后，数据库集群中会包含一个名为 postgres 的数据库，它被用作默认数据库，供工具程序、用户和第三方应用使用。**

👉 这个数据库常作为默认登录目标。例如，你执行 psql -U postgres 时通常就是连接到这个数据库。



---

**每个数据库集群在初始化时还会创建两个数据库，分别是 template1 和 template0。**

👉 这两个是系统模板，用于创建新的数据库。



---

如果您使用的是 PostgreSQL 的预打包版本，它很可能有一个特定的约定来放置数据目录的位置，并且它还可能提供用于创建数据目录的脚本