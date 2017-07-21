## 题目链接 https://vjudge.net/contest/167882

### A - Binary Tree on Plane CodeForces - 277E  <br>
二维平面从上到下多个点 输入坐标判断是否可以形成一个二叉树 输出可以形成的最小总边长<br>
一开始想的是二分匹配/多重匹配 还是图样 没做几道题- - <br>
最小费用最大流：拆点i/i+n 源点0 汇点2*n+1; <br>
0-(1~n) 流量2 费用0  (n+1~2*n)-(2*n+1) 流量1 费用0<br>
foreach i:(1~n) j:(n+1~2*n) ij连边(注意高度大到小) 流量1 费用dis <br>
如果最后流量是n-1 即可以建树 输出费用即可<br>
(并没有判断最高唯一

### B - Okabe and City CodeForces - 821D  <br>
spfa最短路 建图方式使用每个点/每行列间连边做更简单一点 直接建边MLE 故在搜索过程中利用 曼哈顿距离是1还是2 判断<br>

### C - Ciel and Duel CodeForces - 321B <br>




