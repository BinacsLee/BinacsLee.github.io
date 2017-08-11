## 题目链接 https://vjudge.net/contest/167880
BC      <br>
*E*

### A - Assignment HDU - 5289 
输入一个数列 求有多少个连续区间满足区间最大最小值之差小于k<br>
三种解法:<br>
 1. 枚举左端点 二分右端点 用[st算法](http://blog.csdn.net/insistgogo/article/details/9929103 "st")求区间最值
 2. 用单调队列维护最值 (交上去的代码跑的最快)
 3. 用multiset维护区间最值 (最慢) 同队列 自动排序
 
### B - Boring Class HDU - 5324 
题意：给出n个二维点对，求LIS长度和编号字典序最小的LIS（x非增，y非减） <br>
题解：dp[i]=max(dp[j]) (i>j,l[i]>=l[j],r[i]<=r[i]) <br>
一看就是三维偏序问题。<br>
如果树套树写的好，空间开的大的话，一样可以过<br>
本题用cdq分治套树状数组好写一点。todo

### C - Boss Bo HDU - 5756 
可持久化数据结构<br>
题意：给你一个n个点 以1为根的树 Q个询问问你如果把若干个点的子树删掉 剩下的点里面 到P点的距离和 距离的最大值或问距离的最小值<br>
如果点删完了 就输出-1  强制在线的 每次给你一个p 实际的P=(p+lastans)%n +1   lastans是上次的答案 如果是-1或第一组询问 lastans=0<br>
题解：先处理出根节点1到每个点的距离 建一棵可持久化线段树维护和，最大值，最小值，<br>
然后从根节点向下 通过dfs序 对每个点子树里的点权-1 对不在子树里的点权+1 要用静态标记 不用貌似会被卡。<br>
然后对于询问 在P点的主席树上询问删掉的点的子树之外的区间 因为删掉的点的总数不超过20万 所以不会超时 <br>

### D - Danganronpa HDU - 5384 
先输入N个串 再输入M个串 对前N个串中的每个串输出后面M个串在它上面匹配了多少次 M可以重复<br>
AC自动机裸题<br> //todo

### E - Find the Period HDU - 5814  tag
询问子串的最小循环节<br>
论文题：Efficient data structures for the factor periodicity problem.<br>

### F - Good Substrings CodeForces - 271D 
后缀自动机吧应该 好像Trie也能过todo

### G - Hack it! HDU - 5397 
