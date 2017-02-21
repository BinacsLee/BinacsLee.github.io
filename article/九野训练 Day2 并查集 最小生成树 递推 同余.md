## 2017-2-21
## 题目链接 https://vjudge.net/contest/39621 && https://vjudge.net/contest/39794

#### Link 1
    
### A HDU - 1213</br>
并查集</br>
WA 1 </br> 
    
    for(int i=1;i<=k;i++) //wrong 使得后面测试结果出错 应该i=0开始
         father[i]=find(i);
    
    
### B HDU - 1232</br>
并查集

### G POJ - 1789
最小生成树 这几题都用了kruskal算法</br>
注意稠密图最好用prim </br>
WA 1 这道题里一开始father数组开不够RE(因为边太多 n个点 n(n-1)/2条边</br>
WA 2 cnt tot等初始化

### H HDU - 1233 
最小生成树 模版题吧算是</br>
1A了

### I HDU - 1879
部分村庄已经修过路了(即相比上题输入部分加入权值为0的边</br>
处理策略: if(t==1) w=0 然后执行addedge即可</br>
TLE 1 cin超时 改用scanf AC</br>
RE 1 scanf忘了&取地址了...</br>
EXP 1 循环条件maxv别写成maxe... debug蛮傻逼的...</br>

