- **产线集群**：
  - 10.28.62.48 neo4j7.prod.bbdops.com neo4j7 主
  - 10.28.62.49 neo4j8.prod.bbdops.com neo4j8 从
  - 10.28.62.51 neo4j10.prod.bbdops.com neo4j10 从
- **灰度测试集群3.2.6**：
    - wanxiangneo4jpre11 10.28.62.46 http 20011 bolt 30011 主 ssh 10011
    - wanxiangneo4jpre12 10.28.62.47 http 20012 bolt 30012 从 ssh 10012
    - wanxiangneo4jpre13 10.28.62.52 http 20013 bolt 30013 从 ssh 10013
- **灰度测试集群3.4.+**：
    - wanxiangneo4jpre14 10.28.62.46 http 20014 bolt 30014 ssh 10014
    - wanxiangneo4jpre15 10.28.62.47 http 20015 bolt 30015 ssh 10015
    - wanxiangneo4jpre16 10.28.62.52 http 20016 bolt 30016 ssh 10016

- **离线加载专用3.2.6**：
    - wanxiangneo4jpre50 10.28.62.46 http 20050 bolt 30050   ssh 10050

- **灰度API测试容器**：
    - wanxiangneo4japi51 10.28.62.46 http 9999 ssh 10051
    - curl 10.28.62.46:9999/api/0/graph/query?qyId=bc3e060bf3d94692a29bc9c6ecc363f2&distance=8


- **历史库宿主机**：
  - 10.28.62.50 neo4j9.prod.bbdops.com neo4j9

- **历史库宿容器信息 201-212依次对应月份1月-12月**

  - 10.28.62.201	wanxiangneo4jhistory01.prod.bbdops.com  wanxiangneo4jhistory01
  - 10.28.62.202	wanxiangneo4jhistory02.prod.bbdops.com  wanxiangneo4jhistory02
  - 10.28.62.203	wanxiangneo4jhistory03.prod.bbdops.com  wanxiangneo4jhistory03
  - 10.28.62.204	wanxiangneo4jhistory04.prod.bbdops.com  wanxiangneo4jhistory04
  - 10.28.62.205	wanxiangneo4jhistory05.prod.bbdops.com  wanxiangneo4jhistory05
  - 10.28.62.206	wanxiangneo4jhistory06.prod.bbdops.com  wanxiangneo4jhistory06
  - 10.28.62.207	wanxiangneo4jhistory07.prod.bbdops.com  wanxiangneo4jhistory07
  - 10.28.62.208	wanxiangneo4jhistory08.prod.bbdops.com  wanxiangneo4jhistory08
  - 10.28.62.209	wanxiangneo4jhistory09.prod.bbdops.com  wanxiangneo4jhistory09
  - 10.28.62.210	wanxiangneo4jhistory10.prod.bbdops.com  wanxiangneo4jhistory10
  - 10.28.62.211	wanxiangneo4jhistory11.prod.bbdops.com  wanxiangneo4jhistory11
  - 10.28.62.212	wanxiangneo4jhistory12.prod.bbdops.com  wanxiangneo4jhistory12
