# Hey PostgreSQL 100

## macOS

> `15.6`

```bash
brew install postgresql@16
```

```bash
# Intel-based
fish_add_path /usr/local/opt/postgresql@16/bin

# Apple silicon
fish_add_path /opt/homebrew/opt/postgresql@16/bin
```

```
brew services start postgresql@16
```

```bash
psql postgres
```

---

## Ubuntu

> `24.04`

```bash
ansible-galaxy install -r requirements.yml
ansible-playbook playbook.yml
```



---
```bash
sudo su - postgres
psql
```

```bash
sudo -u postgres psql
```

```bash
sudo systemctl status postgresql@16-main.service
```

```
# cat /var/lib/postgresql/16/main/postmaster.opts
/etc/postgresql/15/main/postgresql.conf

# cat /etc/postgresql/16/main/postgresql.conf|grep pg_hba.conf
/etc/postgresql/15/main/pg_hba.conf
```

## Admin

```bash
createuser  ${app_name} -P
createdb -O ${app_name} ${app_name}_production -E UTF8 -e
```



## pg uuid 设置

```bash
CREATE EXTENSION "uuid-ossp";
```



## Ref

* <https://www.postgresql.org/>
* [Community.Postgresql — Ansible Community Documentation](https://docs.ansible.com/ansible/latest/collections/community/postgresql/index.html)