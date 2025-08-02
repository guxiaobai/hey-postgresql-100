# Hey PostgreSQL 100

## macOS

> `15.5`

```bash
brew install postgresql@16
```
> `Intel-based`

```bash
fish_add_path /usr/local/opt/postgresql@16/bin
```
> `Apple silicon`

```bash
fish_add_path /opt/homebrew/opt/postgresql@16/bin
```

```
brew services start postgresql@16
```

```bash
psql postgres
```

## Ubuntu

> `24.04`

```bash
ansible-galaxy install -r requirements.yml
ansible-playbook playbook.yml
```

## Admin

```bash
createuser  ${app_name} -P
createdb -O ${app_name} ${app_name}_production -E UTF8 -e
```

## Ref

* <https://www.postgresql.org/>
* [Community.Postgresql — Ansible Community Documentation](https://docs.ansible.com/ansible/latest/collections/community/postgresql/index.html)