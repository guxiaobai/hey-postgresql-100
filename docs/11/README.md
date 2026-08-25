## 安装 `acl`

> 解决通过非 `root` 切换用户造成的临时文件权限问题

|本期版本|上期版本
|:---:|:---:
`Tue Aug 25 20:23:55 CST 2026` | -

```yml
      become: true
      become_user: postgres
```

[ERROR]: Task failed: Failed to set permissions on the temporary files Ansible needs to create when becoming an unprivileged user (rc: 1, err: chmod: invalid mode: ‘A+user:postgres:rx:allow’
```

## Ref

- <https://docs.ansible.com/projects/ansible/latest/playbook_guide/playbooks_privilege_escalation.html#resolving-temporary-file-error-messages>