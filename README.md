- **灰度HA集群-3.2.6**：

    | 主机IP | 主机名 | http端口 | bolt端口 | 默认角色|
    | :------| :------ | :------ | :------ |:------ |
    | 10.28.62.48 | neo4j7.prod.bbdops.com  | 7474 | 7687 | 主 |
    | 10.28.62.49 | neo4j8.prod.bbdops.com  | 7474 | 7687 | 从 |
    | 10.28.62.51 | neo4j10.prod.bbdops.com | 7474 | 7687 | 从 
    

    
- **万象正式环境-3.4.7**
  
    | 主机IP | 主机名 | http端口 | bolt端口 |
    | :------| :------ | :------ | :------ |
    | 10.28.62.53 | neo4j11.prod.bbdops.com | 7474 | 7687 | 
    | 10.28.62.54 | neo4j12.prod.bbdops.com | 7474 | 7687 | 
    | 10.28.62.55 | neo4j13.prod.bbdops.com | 7474 | 7687 | 
    | 10.28.62.46 | neo4j5.prod.bbdops.com | 7474 | 7687 | 
    | 10.28.62.47 | neo4j6.prod.bbdops.com | 7474 | 7687 | 


- **万象正式环境备用-3.2HA 使用宿主机IP端口访问容器服务 rancher容器**：

    | 容器名 | 宿主机名 | 宿主机IP | http端口 | bolt端口 | ssh端口 | 默认角色|
    | :------| :------ | :------ | :------ | :------ |:------ |:------ |
    |   wanxiangneo4jpre101 | neo4j8.prod.bbdops.com | 10.28.62.49 |  20011 |  30011 | 10011 | 主 |
    |   wanxiangneo4jpre105 | neo4j7.prod.bbdops.com | 10.28.62.48 |  20015 |  30015 | 10015 | 从 |
    |   wanxiangneo4jpre109 | neo4j10.prod.bbdops.com| 10.28.62.51 |  20019 |  30019 | 10019 | 从 |

- **灰度测试集群3.4.+ 使用宿主机IP端口访问容器服务 rancher容器**：

    | 容器名 | 宿主机名 |宿主机IP | http端口 | bolt端口 | ssh端口 | 默认角色|
    | :------| :------ | :------ | :------ | :------ |:------ |:------ |
    |   wanxiangneo4jpre14 | neo4j5.prod.bbdops.com | 10.28.62.46 |  20014 |  30014 | 10014 | 主 |
    |   wanxiangneo4jpre15 | neo4j6.prod.bbdops.com | 10.28.62.47 |  20015 |  30015 | 10015 | 从 |
    |   wanxiangneo4jpre16 | bbd1.prod.bbdops.com | 10.28.62.52 |  20016 |  30016 | 10016 | 从 |

- **离线加载专用 rancher容器**：

    | 容器名 | 宿主机名 | 宿主机IP |http端口 | bolt端口 | ssh端口 | 默认角色| 备注 |
    | :------| :------ | :------ | :------ | :------ |:------ |:------ |:------ |
    |   wanxiangneo4jpre50 | neo4j5.prod.bbdops.com |   10.28.62.46 |  20050 |  30050 | 10050 | 单点 | 停用   |
    |   wanxiangneo4jpre53 | neo4j8.prod.bbdops.com |   10.28.62.49 |  20053 |  30053 | 10053 | 单点 | 3.4.7版本   |
    |   wanxiangneo4jpre54 | neo4j7.prod.bbdops.com |   10.28.62.48 |  20054 |  30054 | 10054 | 单点 | 3.2.6版本   |
    
- **测试环境-3.4.0**：

    | 容器名 | 宿主机名 | 宿主机IP |http端口 | bolt端口 | ssh端口 | 默认角色|
    | :------| :------ | :------ | :------ | :------ |:------ |:------ |
    |   wanxiangneo4jtest1 | CT11 |   10.28.102.29 |  17474 |  17687 | 52668 | 单点 |

- **测试环境-3.2.6**：

    | 容器IP | 容器名  | http端口 | bolt端口 | 宿主机名 | 宿主IP |
    | :------| :------ | :------ | :------  | :------ | :------ |
    | 10.28.102.31 | wanxiang102neo4j1 | 7474 | 7687  | CT9 | 10.28.102.19 |
    | 10.28.102.32 | wanxiang102neo4j2 | 7474 | 7687  | CT9 | 10.28.102.19 |

- **历史库宿容器信息 201-212依次对应月份1月-12月, 直接使用容器IP和端口访问服务, 在网桥模式的neo4j9上,shell或ssh访问**

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

- **历史库宿容器信息-3.4.7**

    | 容器IP | 容器名  | http端口 | bolt端口 | 宿主机名 | 宿主IP |
    | :------| :------ | :------ | :------  | :------ | :------ |
    | 10.42.62.201 | wanxiangneo4jhistory01.prod.bbdops.com | 7474 | 7687  | neo4j7.prod.bbdops.com | 10.28.62.48 |
    | 10.42.62.202 | wanxiangneo4jhistory02.prod.bbdops.com | 7474 | 7687  | neo4j7.prod.bbdops.com | 10.28.62.48 |
    | 10.42.62.203 | wanxiangneo4jhistory03.prod.bbdops.com | 7474 | 7687  | neo4j7.prod.bbdops.com | 10.28.62.48 |
    | 10.42.62.204 | wanxiangneo4jhistory04.prod.bbdops.com | 7474 | 7687  | neo4j7.prod.bbdops.com | 10.28.62.48 |
    | 10.42.62.205 | wanxiangneo4jhistory05.prod.bbdops.com | 7474 | 7687  | neo4j8.prod.bbdops.com | 10.28.62.49 |
    | 10.42.62.206 | wanxiangneo4jhistory06.prod.bbdops.com | 7474 | 7687  | neo4j8.prod.bbdops.com | 10.28.62.49 |
    | 10.42.62.207 | wanxiangneo4jhistory07.prod.bbdops.com | 7474 | 7687  | neo4j8.prod.bbdops.com | 10.28.62.49 |
    | 10.42.62.208 | wanxiangneo4jhistory08.prod.bbdops.com | 7474 | 7687  | neo4j8.prod.bbdops.com | 10.28.62.49 |
    | 10.42.62.209 | wanxiangneo4jhistory09.prod.bbdops.com | 7474 | 7687  | neo4j10.prod.bbdops.com | 10.28.62.51 |
    | 10.42.62.210 | wanxiangneo4jhistory10.prod.bbdops.com | 7474 | 7687  | neo4j10.prod.bbdops.com | 10.28.62.51 |
    | 10.42.62.211 | wanxiangneo4jhistory11.prod.bbdops.com | 7474 | 7687  | neo4j10.prod.bbdops.com | 10.28.62.51 |
    | 10.42.62.212 | wanxiangneo4jhistory12.prod.bbdops.com | 7474 | 7687  | neo4j10.prod.bbdops.com | 10.28.62.51 |
- 
**历史库冷备**
  - backup07 /tank/hadoop/neo4j/wanxiang/neo4j_prod_history_backup
  - 历史库备份当中保留所有历史版本，每次有新历史库，同时同步到neo4j9对应容器和历史库冷备当中。现阶段约定,在neo4j9上只运行最近6个月的库

