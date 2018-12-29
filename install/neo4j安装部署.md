#### neo4j安装部署文档



一：环境依赖及要求
 > * 1：cpu最低限度Intel Core i3
 > * 2：推荐Intel Core i7 或者 IBM POWER8
 > * 3：内存至少2G
 > * 4：磁盘最少10G sata
 > * 5: 文件系统最低EXT4
 > * 6：java8及以上

 官方参考：https://neo4j.com/docs/operations-manual/3.5/installation/requirements/

-------------------------------------------------------------------

二：下载安装包
> * 官网下载对应的二进制包  地址：https://neo4j.com/download/

-------------------------------------------------------------------


三：解压

> * tar -zxvf  neo4j-enterprise-3.4.7-unix.tar.gz

 -----------------------------------------------------------
 
 
四：配置
vim conf/neo4j.conf
```
dbms.active_database=graph.db   //库名
dbms.backup.enabled=true
dbms.backup.address=10.42.40.11:6362   
dbms.connectors.default_listen_address=10.42.40.11
dbms.connectors.default_advertised_address=10.42.40.11
dbms.connector.bolt.enabled=true
dbms.connector.bolt.listen_address=10.42.40.11:7687
dbms.connector.http.enabled=true
dbms.connector.http.listen_address=10.42.40.11:7474
dbms.threads.worker_count=2000
dbms.tx_log.rotation.retention_policy=1 days
dbms.shell.enabled=true
dbms.shell.host=10.42.40.11
dbms.shell.port=1337
dbms.jvm.additional=-XX:+UseG1GC
dbms.jvm.additional=-XX:-OmitStackTraceInFastThrow
dbms.jvm.additional=-XX:+AlwaysPreTouch
dbms.jvm.additional=-XX:+UnlockExperimentalVMOptions
dbms.jvm.additional=-XX:+TrustFinalNonStaticFields
dbms.jvm.additional=-XX:+DisableExplicitGC
dbms.jvm.additional=-Djdk.tls.ephemeralDHKeySize=2048
dbms.windows_service_name=neo4j
dbms.jvm.additional=-Dunsupported.dbms.udc.source=tarball

对应的ip改成本机ip地址
```


-----------------------------------------------------------

五：修改图库默认密码
启动前执行
`./bin/neo4j-admin set-initial-password your-password`

-----------------------------------------------------------


六：启动图库
`./bin/neo4j start `

-----------------------------------------------------------


七：界面登录验证
 http://x.x.x.x:7474/browser/