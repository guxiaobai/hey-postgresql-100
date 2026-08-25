
```yml
      become: true
      become_user: postgres
```

[ERROR]: Task failed: Failed to set permissions on the temporary files Ansible needs to create when becoming an unprivileged user (rc: 1, err: chmod: invalid mode: ‘A+user:postgres:rx:allow’
```

## 解决办法安装 `acl`