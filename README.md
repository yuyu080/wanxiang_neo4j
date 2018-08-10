- **产线集群**：

    | 主机IP | 主机名 | http端口 | bolt端口 | 默认角色|
    | :------| :------ | :------ | :------ |:------ |
    | 10.28.62.48 | neo4j7.prod.bbdops.com  | 7474 | 7687 | 主 |
    | 10.28.62.49 | neo4j8.prod.bbdops.com  | 7474 | 7687 | 从 |
    | 10.28.62.51 | neo4j10.prod.bbdops.com | 7474 | 7687 | 从 
    
- **5节点灰度环境-3.4.0 rancher容器**
  
    | 主机IP | 主机名 | http端口 | bolt端口 |
    | :------| :------ | :------ | :------ |
    | 10.28.62.53 | neo4j11.prod.bbdops.com | 7474 | 7687 | 
    | 10.28.62.54 | neo4j12.prod.bbdops.com | 7474 | 7687 | 
    | 10.28.62.55 | neo4j13.prod.bbdops.com | 7474 | 7687 | 
    | 10.28.62.46 | neo4j5.prod.bbdops.com | 7474 | 7687 | 
    | 10.28.62.47 | neo4j6.prod.bbdops.com | 7474 | 7687 | 


- **灰度测试集群3.2.6 使用宿主机IP端口访问容器服务 rancher容器**：

    | 容器名 | 宿主机名 | 宿主机IP | http端口 | bolt端口 | ssh端口 | 默认角色|
    | :------| :------ | :------ | :------ | :------ |:------ |:------ |
    |   wanxiangneo4jpre11 | neo4j5.prod.bbdops.com | 10.28.62.46 |  20011 |  30011 | 10011 | 主 |
    |   wanxiangneo4jpre12 | neo4j6.prod.bbdops.com | 10.28.62.47 |  20012 |  30012 | 10012 | 从 |
    |   wanxiangneo4jpre13 | bbd1.prod.bbdops.com | 10.28.62.52 |  20013 |  30013 | 10013 | 从 |

- **灰度测试集群3.4.+ 使用宿主机IP端口访问容器服务 rancher容器**：

    | 容器名 | 宿主机名 |宿主机IP | http端口 | bolt端口 | ssh端口 | 默认角色|
    | :------| :------ | :------ | :------ | :------ |:------ |:------ |
    |   wanxiangneo4jpre14 | neo4j5.prod.bbdops.com | 10.28.62.46 |  20014 |  30014 | 10014 | 主 |
    |   wanxiangneo4jpre15 | neo4j6.prod.bbdops.com | 10.28.62.47 |  20015 |  30015 | 10015 | 从 |
    |   wanxiangneo4jpre16 | bbd1.prod.bbdops.com | 10.28.62.52 |  20016 |  30016 | 10016 | 从 |

- **离线加载专用3.2.6 rancher容器**：

    | 容器名 | 宿主机名 | 宿主机IP |http端口 | bolt端口 | ssh端口 | 默认角色|
    | :------| :------ | :------ | :------ | :------ |:------ |:------ |
    |   wanxiangneo4jpre50 | neo4j5.prod.bbdops.com |   10.28.62.46 |  20050 |  30050 | 10050 | 单点 |

- **灰度API测试容器 rancher容器**：

    | 容器名 | neo4j版本 | 宿主机名 | 宿主机IP | http端口  | ssh端口 | 测试URL|
    | :------| :------ | :------ |:------ | :------ |:------ |:------ |
    |   wanxiangneo4japi51 | neo4j3.2 | neo4j5.prod.bbdops.com | 10.28.62.46 |  9999 | 10051 | curl 10.28.62.46:9999/api/0/graph/query?qyId=bc3e060bf3d94692a29bc9c6ecc363f2&distance=8 |
    |   wanxiangneo4japi52 | neo4j3.4 | neo4j6.prod.bbdops.com | 10.28.62.47 |  9999 | 10052 |  |

- **历史库宿容器信息 201-212依次对应月份1月-12月, 直接使用容器IP和端口访问服务，在网桥模式的neo4j9上,shell或ssh访问**

    | 容器IP | 容器名  | http端口 | bolt端口 | 宿主机名 | 宿主IP |
    | :------| :------ | :------ | :------  | :------ | :------ |
    | 10.28.62.201 | wanxiangneo4jhistory01.prod.bbdops.com | 7474 | 7687  | neo4j9.prod.bbdops.com | 10.28.62.50 |
    | 10.28.62.202 | wanxiangneo4jhistory02.prod.bbdops.com | 7474 | 7687  | neo4j9.prod.bbdops.com | 10.28.62.50 |
    | 10.28.62.203 | wanxiangneo4jhistory03.prod.bbdops.com | 7474 | 7687  | neo4j9.prod.bbdops.com | 10.28.62.50 |
    | 10.28.62.204 | wanxiangneo4jhistory04.prod.bbdops.com | 7474 | 7687  | neo4j9.prod.bbdops.com | 10.28.62.50 |
    | 10.28.62.205 | wanxiangneo4jhistory05.prod.bbdops.com | 7474 | 7687  | neo4j9.prod.bbdops.com | 10.28.62.50 |
    | 10.28.62.206 | wanxiangneo4jhistory06.prod.bbdops.com | 7474 | 7687  | neo4j9.prod.bbdops.com | 10.28.62.50 |
    | 10.28.62.207 | wanxiangneo4jhistory07.prod.bbdops.com | 7474 | 7687  | neo4j9.prod.bbdops.com | 10.28.62.50 |
    | 10.28.62.208 | wanxiangneo4jhistory08.prod.bbdops.com | 7474 | 7687  | neo4j9.prod.bbdops.com | 10.28.62.50 |
    | 10.28.62.209 | wanxiangneo4jhistory09.prod.bbdops.com | 7474 | 7687  | neo4j9.prod.bbdops.com | 10.28.62.50 |
    | 10.28.62.210 | wanxiangneo4jhistory10.prod.bbdops.com | 7474 | 7687  | neo4j9.prod.bbdops.com | 10.28.62.50 |
    | 10.28.62.211 | wanxiangneo4jhistory11.prod.bbdops.com | 7474 | 7687  | neo4j9.prod.bbdops.com | 10.28.62.50 |
    | 10.28.62.212 | wanxiangneo4jhistory12.prod.bbdops.com | 7474 | 7687  | neo4j9.prod.bbdops.com | 10.28.62.50 |

- **历史库备份**
  - backup07 /tank/hadoop/neo4j/wanxiang/neo4j_prod_history_backup