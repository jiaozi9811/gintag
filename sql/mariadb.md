## install mariadb

```apt install mariadb-server mariadb-client```

```mysql_secure_installation```

```
grant all privileges on *.* to root@'%' identified by "";
FLUSH PRIVILEGES;
```

## 开启远程服务
1. 注释掉skip-networking选项来开启远程访问.
2. 注释bind-address项，该项表示运行哪些IP地址的机器连接

```
grep -rn "skip-networking" .
grep -rn "bind-address" .
./mariadb.conf.d/50-server.cnf
````