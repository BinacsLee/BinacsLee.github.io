### 2017-02-14
### 题目链接 https://vjudge.NET/contest/149929

## A poj2139
N个奶牛共参演M个电影 第一行输入N和M
第2-M+1行输入第i个电影参演的奶牛编号 度数与奶牛间关联有关(最短路 
输出拥有平均最短路的奶牛的平均最短路*100
Floyd-Warshall O(N^3)  (通常n<=200 这300也可以了
WA1没有乘100= =


## B poj3259
N个农场内有M个路径(双向)和W个虫洞(单向负权) 求在该农场内能否走某条路径(回路 使总权值负(时间比之前到这早
有输出YES 没有NO
判断图是否存在负权环
Solution 1 Bellman-Ford判定(挑战程序设计竞赛//todo
Solution 2 spfa 上述算法使用队列优化
Solution 3 Floyd-Warshall O(N^3) //todo
EXP 1算法实现细节= =


## C poj3268
N个农场N条牛 每个牛去牛x那里然后返回 农场间为有向通道
输出去-返回路径长度总和最大的值
Dijkstra (spfa 但bf计算量较大超时
返回:单源最短路
去:矩阵转置后 单源最短路


## D poj1258
最小生成树
标准Prim


## E poj2377
最大生成树
记录负权使用Prim ／ Dijkstra


## F poj2395
求最小生成树的最大权的边 (有重边
Solution 1 重边 故dijkstra
Solution 2 二分边权


'''
授课内容
一 概念
1 平面图 可平面图 
2 哈密顿回路(边 欧拉回路(点
3 LCA(Least Common Ancestors) ST算法(在线),Tarjan算法(离线)
4 偶图/二分图 匹配 强连通分量(两两可达 弱连通分量(有向改无向后两两可达 
5 图论中特殊集合 点覆盖集边覆盖集 
     独立集(一个边集,使得所有点都与集合里的边邻接)   支配集(一个边集,使得所有点都与集合里的边邻接)
     最小路径覆盖(path covering)(用尽量少的不相交简单路径覆盖有向无环图G的所有顶点(每个顶点严格属于一条路径))
二 主要算法
1 搜索 (dfs bfs 模拟退火 A*
2 拓扑排序 (DAG 可以DP    具体算法:队列实现
3 强连通分量 (Tarjan算法求LCA和强连通分量) //todo
4 最小生成树 (Prim Kruskal
5 最短路 （Bellman-Ford , Dijkstra , Floyd , SPFA算法
6 网络流/费用流 (DINIC算法 , SPFA解决费用流
7 二分图匹配/一般图匹配 (匈牙利算法 , KM算法 , 带花树算法

'''

找个时间找下算法模版= = 手写能力还是太弱了QAQ
