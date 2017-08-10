## 题目链接 https://vjudge.net/contest/167878#problem
BCG

### A - Arif in Dhaka (First Love Part 2) UVA - 10294 
polya定理 <br>
考虑旋转 t^a(a是转i个珠子时的循环节个数=gcd(n,i))求和 最后除n(取平均数)<br>
考虑对称 如果n是奇数 n*2^((n+1)/2) 偶数 n/2*(2^(n/2)+a^(n/2+1)) 最后除2再除n <br>

### B - Expensive Drink HDU - 2979 
<br>什么三维线性规划 单纯形 啥？
<br> //todo
<br>

### C - Battle for the Ring URAL - 1540 
SG (和记忆化搜索？？)

### D - Little Elephant and Triangle CodeForces - 220D 
0-w 0-h的平面 选择整数点作面积非零且为整数的三角形 问能做出多少个 三个点变换顺序算不同<br>
数学 可以再看看

### E - Divisibility Rules CodeForces - 180B 
      * 能被2整除的数的规则：一个数能被2整除当且仅当它的最后一位能被2整除，或者换句话说，是偶数。
      * 能被3整除的数的规则：一个数能被3整除当且仅当它的各个数位上的数字之和能被3整除。
      * 能被4整除的数的规则：一个数能被4整除当且仅当它的最后两位形成的数能被4整除。
      * 能被5整除的数的规则：一个数能被5整除当且仅当它的最后一位是5或0。
      * 能被6整除的数的规则：一个数能被6整除当且仅当它能同时被2和3整除（也就是说，当且仅当它的最后一位是偶数而且各个数位上的数字之和能被3整除）
      * 能被7整除的数的规则：Vasya不知道这个整除性质。
      * 能被8整除的数的规则：一个数能被8整除当且仅当它的最后三位形成的数能被8整除。
      * 能被9整除的数的规则：一个数能被9整除当且仅当它的各个数位上的数字之和能被9整除。
      * 能被10整除的数的规则：一个数能被10整除当且仅当它的最后一位是0。
      * 能被11整除的数的规则：一个数能被11整除当且仅当它的奇数位上的数字之和等于它的偶数位上的数字之和，或者它们相差一个能被11整除的数。
      检查一个数能否被2,4,5,8,10整除的时候只需要检查它的最后一位或几位是否满足某个条件。Vasya把这种规则称为2类型规则(2-type)。
      
      如果检查一个数能否被给定的数整除意味着计算这个数的各个数位上的数字之和并判断这个和能否被给定的数整除，那么Vasya称这个规则为3类型规则（3-type）（因为它对3和9有效）
      
      如果我们需要求出一个数的奇数位上的数字之和与偶数位上的数字之和的差值去检查这个差值能否被给定数整除，那么这个规则被称为11类型规则（11-type）（它对11有效）。
      有些情况下我们应当把除数分解成一些因数然后检查是否满足一些不同类型的规则（2-type,3-type,11-type）。例如，对于除数6我们需要检查2-type和3-type规则，对于除数66我们检查所有的三种类型的规则。这样混合的整除规则被称为6类型规则(6-type)。
      最后，有些除数是所有类型的规则都无效的：既不是2-type，也不是3-type，也不是11-type，也不是6-type。这样的数最小的是7，所以我们称在这种情况下神秘的7类型规则(7-type)有效，也就是那种Vasya还没有发现的类型。
      
假设进制数b 除数d 

      while((g=gcd(b,d))>1) d/=g,c++;
      if(d==1) printf("2-type\n%d",c);
      else if(!c&&b%d==1) printf("3-type\n");
      else if(!c&&b%d==d-1) printf("11-type\n");
      else if((b*b-1)/(b%2+1)%d==0) printf("6-type\n");
      else printf("7-type\n");
      
### F - Bear in the Field CodeForces - 385E 
考虑熊移动有一定的规律性/可以规律表示<br>
矩阵快速幂 构造矩阵即可<br>
矩阵struct不初始化0也会WA... 注意了 标准化过程
### G - Smart Cheater CodeForces - 150C 
线段树//todo
### H - Subway Innovation CodeForces - 371E 
输入包含n个车站的一维坐标 目的是留下k个车站使得k个车站两两之间的距离和最小 输出这k个车站的输入编号<br>
直观易知 这k个车站是连续车站应该是最优解 接下来要找以哪个为起点的连续k个车站是所求答案<br>
直接暴力O(nk)要T 现考虑起点从左向右移动时结果的变化<br>
显然利用前缀和即可

### I - The Elder Trolls IV: Oblivon CodeForces - 73A 
把x*y*z的三维物体切割k次(按面割) 最多可以切成多少块

         while(x+y+z-3>k){
             ll t=max(x,max(y,z));
             if(t==x) x--;
             else if(t==y) y--;
             else z--;
         }
         printf("%lld\n",x*y*z);
      
 ### J - Watching Fireworks is Fun CodeForces - 372C 
 dp+单调队列//todo
 ### K - Playing with Permutations CodeForces - 251B 
      #
      #
      
