## 题目链接 https://vjudge.net/contest/167882

DFGIJ
### A - Binary Tree on Plane CodeForces - 277E  <br>
二维平面从上到下多个点 输入坐标判断是否可以形成一个二叉树 输出可以形成的最小总边长<br>
一开始想的是二分匹配/多重匹配 还是图样 没做几道题- - <br>
最小费用最大流：拆点i/i+n 源点0 汇点2*n+1; <br>
0 - (1 ~ n) 流量2 费用0  (n+1 ~ 2*n) - (2*n+1) 流量1 费用0<br>
foreach i:(1 ~ n) j:(n+1 ~ 2*n) ij连边(注意高度大到小) 流量1 费用dis <br>
如果最后流量是n-1 即可以建树 输出费用即可<br>
(并没有判断最高唯一

### B - Okabe and City CodeForces - 821D  <br>
spfa最短路 建图方式使用每个点/每行列间连边做更简单一点 直接建边MLE 故在搜索过程中利用 曼哈顿距离是1还是2 判断<br>

### C - Ciel and Duel CodeForces - 321B <br>
卡牌攻击<br>
贪心： 分两种情况
1. 没有造成抵消后的完整伤害 显然此时最大的B对最小的Aatt可使总结果最大
2. 造成了完整伤害 则从AdefAatt左开始扫描 循环cnt3++ 先判是否满足大于Adef else判和Aatt else完整伤害 若cnt1 cnt2个都达到 flag=true
3. flag=true则输出二者最大值 否则输出第一个计算结果

### E - Scheme CodeForces - 22E
求图加上多少边形成强连通图<br>
(因为对输出有要求 故第一次从入度为0的点dfs求连通量后记录末尾点st ed 相当于缩点)<br>
第二次从未被访问过的点开始dfs 继续记录st和ed<br>
最后把这些点加上边即可(注意dfs里col数组用法)<br>

### F 没人做//todo

<br>

### G - Dual Core CPU POJ - 3469 
最小割 //todo

### H - Word Rings UVALive - 3531 
字符串头俩字符与后俩字符连边 边长为字符串长度(>=2) 要求能够形成的和最大的正环<br>
二分枚举+spfa判环 注意这里spfa的写法<br>

### I - Double NP-hard UVA - 10984 
好像没啥人做//todo
<br><br>
### J - The Great Wall Game UVALive - 3276 

