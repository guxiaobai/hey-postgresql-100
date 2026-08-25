
修改密码

```bash
ALTER USER postgres WITH PASSWORD 'password';
```


## 使用 `.pgpass` 文件（安全且方便）

```bash
echo "192.168.100.81:5432:postgres:postgres:你的密码" > ~/.pgpass

# WARNING: password file "/Users/lemon/.pgpass" has group or world access; permissions should be u=rw (0600) or less
chmod 600 ~/.pgpass
```

## 验证远程连接

```sql
SELECT current_user;
```