- **产线集群**：

    | 主机IP | 主机名 | http端口 | blot端口 | 默认角色|
    | :------| :------ | :------ | :------ |:------ |
    | 10.28.62.48 | neo4j7.prod.bbdops.com  | 7474 | 7687 | 主 |
    | 10.28.62.49 | neo4j8.prod.bbdops.com  | 7474 | 7687 | 从 |
    | 10.28.62.51 | neo4j10.prod.bbdops.com | 7474 | 7687 | 从 |

- **灰度测试集群3.2.6**：

    | 容器名 | 宿主机IP | http端口 | blot端口 | ssh端口 | 默认角色|
    | :------| :------ | :------ | :------ |:------ |:------ |
    |   wanxiangneo4jpre11 | 10.28.62.46 |  20011 |  30011 | 10011 | 主 |
    |   wanxiangneo4jpre12 | 10.28.62.47 |  20012 |  30012 | 10012 | 从 |
    |   wanxiangneo4jpre13 | 10.28.62.52 |  20013 |  30013 | 10013 | 从 |

- **灰度测试集群3.4.+**：

    | 容器名 | 宿主机IP | http端口 | blot端口 | ssh端口 | 默认角色|
    | :------| :------ | :------ | :------ |:------ |:------ |
    |   wanxiangneo4jpre14 | 10.28.62.46 |  20014 |  30014 | 10014 | 主 |
    |   wanxiangneo4jpre15 | 10.28.62.47 |  20015 |  30015 | 10015 | 从 |
    |   wanxiangneo4jpre16 | 10.28.62.52 |  20016 |  30016 | 10016 | 从 |

- **离线加载专用3.2.6**：

    | 容器名 | 宿主机IP | http端口 | blot端口 | ssh端口 | 默认角色|
    | :------| :------ | :------ | :------ |:------ |:------ |
    |   wanxiangneo4jpre50 | 10.28.62.46 |  20050 |  30050 | 10050 | 单点 |

- **灰度API测试容器**：

    | 容器名 | 宿主机IP | http端口  | ssh端口 | 测试URL|
    | :------| :------ | :------  |:------ |:------ |
    |   wanxiangneo4japi51 | 10.28.62.46 |  9999 | 10051 | curl 10.28.62.46:9999/api/0/graph/query?qyId=bc3e060bf3d94692a29bc9c6ecc363f2&distance=8 |

- **历史库宿容器信息 201-212依次对应月份1月-12月**

    | 容器IP | 容器名  | http端口 | blot端口 | 宿主机名 | 宿主IP |
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