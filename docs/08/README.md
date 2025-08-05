# 08 Connection Settings



> `/etc/postgresql/16/main/postgresql.conf`



`listen_addresses` (`string`)



取值|说明
---|---
`*` | 所有可用的 IP 接口
`0.0.0.0` | IPv4
`::` | IPv6



## Ref



* <https://www.postgresql.org/docs/16/runtime-config-connection.html#GUC-LISTEN-ADDRESSES>