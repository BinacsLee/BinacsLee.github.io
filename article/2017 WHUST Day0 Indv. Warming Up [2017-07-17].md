## 题目链接 https://vjudge.net/contest/167876#problem/

E F G H I


### A - Straight «A» CodeForces - 810A 
给定一系列分数 要所有分数的平均分不少于k-0.5 每一课都可以加个数 求这个数 简单模拟即可

### B - Vladik and Courtesy CodeForces - 811A 
每个人轮流减 谁先小于0 输出即可

### C - Summer sell-off CodeForces - 810B 
一系列天 这些天每天有多少货 每天能卖多少货 可以选f天让货量翻倍 求最多能卖多少<br>
输入的时候 1先res+=不翻倍时能卖的最大数 顺便存入假设把当前天翻倍能多卖的个数 再排序扫一遍即可<br>
但是没明白直接排序后再统一计算res会wa在test8 贪心策略不对?

### D - Vladik and Complicated Book CodeForces - 811B 
对一个序列的某个区间操作 每次操作会把这段区间按升序排列 求问排列后某个位置的页是否不变 各个操作相互独立<br>
如果直接模拟再sort排序显然TLE 简单方法是统计该区间有多少比这页小的数 那么这页在排序后的位置即确定 即可

### E - Vladik and Memorable Trip CodeForces - 811C 
<br>
<br>  //todo
<br>

### F - Do you want a date? CodeForces - 810C 
n个数组成的2^n个集合 问每个集合最大值减最小值的和 mod(1e9+7) <br>
暴力O(n^2)超时 可以试图计算每个数据加／减多少次 (2^(i-1) 2^(n-i)) O(n)解决

### G - Glad to see you! CodeForces - 810D 
<br> 二分+交互
<br> //todo 
<br>
### H - Vladik and Favorite Game CodeForces - 811D 
做过 然而Idleness limit exceeded啥子鬼 只能do it again了..

### I - Find a car CodeForces - 810E 
<br>数位dp
<br>//todo
<br>
### J - Vladik and Entertaining Flags CodeForces - 811E 
线段树+并查集
