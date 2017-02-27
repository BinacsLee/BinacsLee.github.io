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

### C HDU - 1272</br>
并查集</br>
WA 1 输入都为0 0 时应输出Yes

### D HDU - 3461
y并查集+快速幂取模</br>

### E HDU - 3172
map+并查集</br>
WA 1 
    
    
    return father[x]=find(father[x]);//find 函数中使用路经压缩 否则TLE到死
    
    
    for(int i=1;i<=100000;i++){   //写成了for(int i=1;i<=2*n;i++) 同样TLE
         num[i]=1;father[i]=i;
    }
    
    
    
### F HDU - 3038//todo

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

### J HDU - 3938
离线化并查集</br>
//todo

### KLMNOPQ
//todo

### RSTUVWX
hdu汉诺塔系列</br>
http://blog.csdn.net/xueerfei008/article/details/9904681
 1. 多柱汉诺塔 <多柱汉诺塔最优算法设计探究> http://www.cnblogs.com/fanzhidongyzby/archive/2012/07/28/2613173.html
    //用pow函数返回的是一个double类型 min函数里比较也是用double 最后赋值的时候取int型 
 2. 普通汉诺塔 总的移动次数(最优 是 2^n-1  相邻的俩盘子上面盘子移动次数是下面的两倍 最下面1
    //关于超长整数表示的问题 此题cout直接输出pow结果WA 因为pow输出为 1.234*e12 这样 不是标准整数 应printf("%.0f"...或者??
 3. 普通汉诺塔(n个盘 最少移动次数是2^n-1,即在移动过程中会产生2^n个系列。
    发生错移产生的系列就增加了 这种错误是放错了柱子 并不会把大盘放到小盘上 n=m+p+q 求系列总数 即
    n个盘子 每个盘子有3种摆法 所以n个盘子摆在3个塔上的摆法就有3^n种
 4. 给定某一时刻的三个柱子上的盘子 问其是不是符合最优解过程中某一时刻的状态
    //http://blog.csdn.net/z690933166/article/details/8605261
 5. 改变游戏的玩法 不允许直接从最左(右)边移到最右(左)边(每次移动一定是移到中间杆或从中间移出) 也不允许大盘放到下盘的上面 
    至少多少次移动才能把这些圆盘从最左边移到最右边
    //递推 num[i]=3*num[i-1]+2;
 6. 5的基础上只允许最大的盘子放到最上面
    f[1]=2;f[2]=4;
    for(i=3; i<=21; i++) f[i]=f[i-1]+6*(f[i-2]-1);
 7. 普通汉诺塔,问在最优步骤中的第i步是哪一个盘子 
    就是奇数倍的2^(i-1)时，i号盘子会移动
 8. 普通汉诺塔 N个盘子 在最优解的第M步时 每个柱子上的盘子的状态
    //http://blog.lchx.me/index.php/hdu-2184-%E6%B1%89%E8%AF%BA%E5%A1%94viii/
 9. 进一步加强条件 在求第m步时是哪个盘子动 怎么动 
    //上面修改一下
 10. 很O_O的汉诺塔 http://blog.csdn.net/murmured/article/details/9943947


