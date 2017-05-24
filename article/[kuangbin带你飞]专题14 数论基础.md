## 链接 https://vjudge.net/contest/70017

##### B L P Q T X Z<br>


### A - Bi-shoe and Phi-shoe LightOJ - 1370</br>
素数表略 比输入大的第一个素数
<br><br>
### B    todo </br>
todo<br>

<br><br>

### C - Aladdin and the Flying Carpet LightOJ - 1341  </br>
唯一分解定理 素数
<br><br>
### D - Sigma Function LightOJ - 1336   </br>  mark
背景: 给定正整数n 其因式分解为 p1^e1 * p2^e2 * -- *pk^ek<br>
则n的所有约数之和可用公式表示为f(n) [(p1^(e1+1) - 1)/(p1-1)]* .. <br>
现输入n 输出从1到n 的f(i)值为偶数的个数<br>
思路 若f(i)为奇数 必为平方数或者平方数的二倍 <br>
故 ans=n-(ll)sqrt(n)-(ll)sqrt(n/2); //注意加ll 否则wa <br>

<br><br>
### E - Leading and Trailing LightOJ - 1282  </br>
获取a^n的前三位和后三位</br>
后三位显然利用快速幂 前三位则利用内置log函数</br>
    
    cin>>a>>n;
    double p=pow(10.0,fmod(n*log10(1.0*a),1));  //其中fmod( ... , 1 )获取小数位
    p=p*100;
        //上述 n*log10(1.0*a) 的整数位表示数据位数 后面表示具体数值
    
<br><br>
### F - Goldbach`s Conjecture LightOJ - 1259  </br>
哥德巴赫猜想相关 给定偶数求分解成两个素数的'种类'数 暴力遍历即可
<br><br>
### G - Harmonic Number (II) LightOJ - 1245  </br>
找规律推公式 这个大概可以记下来吧
    
    //要求下列
    long long H( int n ) {
        long long res = 0;
        for( int i = 1; i <= n; i++ )
            res = res + n / i;
        return res;
    }
    
    ll ans=0;
    ll i=1;
    while(i<=n){
        ans+=(n/(n/i)-i+1)*(n/i);
        i=n/(n/i)+1;
    }
    
    
<br>
网上也有分块加速、或者利用图像 先
    
    sum+=n/i;   //for
    sum*=2;
    sum-=(i-1)*(i-1) //也即i-1=sqrt(n);
    
<br><br>
### H - Pairs Forming LCM LightOJ - 1236  </br>
给你一个数n,让你求满足lcm(a,b)=n的a,b的对数 (算数基本定理相关)<br>
<br><br>
### I - Harmonic Number LightOJ - 1234  </br>
打表技巧规律 给你一个n,让你求1/1+1/2+1/3+..1/n 可以隔50记录一次 但是有公式
    
    da[1]=1.0;
    for(int i=2;i<=100000;i++){
        da[i]=da[i-1]+1.0/i;
    }
    //调和级数 小的时候可以暴力 对于大数 利用公式
    
    const double C=0.57721566490153;
    double res=log(n)+1.0/(2.0*n)+C;
    
    

    
<br><br>
### J - Mysterious Bacteria LightOJ - 1220  </br>
给你一个整数n(可能为负数 wa了在这),让你求满足a^p=n的最大的p<br>
因式分解 然后求所有素因子次数的最大公约数 如果n负数还要把所得结果除到是奇数为止<br>
 !!! 注意
    
    
    ll ans=0,m=sqrt(nn+0.5);  //使用素数表防超时
    for(ll i=0;i<cnt&&prime[i]<=m;i++) if(nn%prime[i]==0){
        ll tem=0;
        while(nn%prime[i]==0) {nn/=prime[i];tem++;}
        if(tem) {if(!ans) ans=gcd(ans,tem);else ans=tem;}
    }
    if(nn!=1) ans=gcd(ans,1);   // 注意！！！ 如果n本身就是素数(m<n) 最后不为1的情况 
    
    
<br><br>
### K - Large Division LightOJ - 1214  </br>
模拟大数除法 看能不能除尽 好像可以直接ll？  (是的 <br>
这种模拟除法的 可以直接从头取余啊...
    
    for(int i=0;i<s.length();i++){
        if(s[i]=='-') continue;
        res=(res*10+s[i]-'0')%b;
    }
    
    
<br><br>
### L - Fantasy of a Summation LightOJ - 1213       todo</br>
给一个求和循环 计算最终结果 规律+快速幂 <br>
todo<br>
<br><br>
### M - Help Hanzo LightOJ - 1197  Mark </br>
区间筛素数 数比较大<br>
先生成素数表 然后<br>
    
    //这个要记住...
    memset(tt,0,sizeof(tt));
    for(int i=0;i<cnt&&(LL)prim[i]*prim[i]<=b;i++){  
         LL st=max(a/prim[i]*prim[i],(LL)prim[i]*prim[i]);  
         for(LL j=st;j<=b;j+=prim[i])  if(j>=a)  tt[j-a]=1;  
    } 
    
<br><br>

### N	LightOJ 1138	Trailing Zeroes (III)  <br>
尾数为0的个数 因式分解(5、2)  二分查找<br>

<br><br>
### O	UVA 11426	GCD - Extreme (II) <br>
欧拉函数表 打表离线输出<br>

<br><br>
### P	UVA 11754	Code Feat	      todoagain   <br>
中国剩余定理基础上 有点复杂<br>
todo<br>
<br><br>
### Q	UVA 11916	Emoogle Grid   todo  <br>
离散对数？<br>
todo<br>

<br><br>
### R - 青蛙的约会 POJ - 1061   <br>
拓展欧几里得<br>

<br><br>
### S - C Looooops POJ - 2115  <br>
拓展欧几里得<br>

<br><br>

### T - Death to Binary? POJ - 2116  todo <br>
todo<br>

<br><br>
### U - Primes HDU - 2161 <br>
判断是不是素数 打表即可 <br>

<br><br>
### V - Maximum GCD UVA - 11827 <br>
求一行数据中两两数字的最大公约数的最大值 输入需要处理<br>
    
    string str;
    getline(cin,str);
    stringstream stream(str);
    int cnt=0;
    while(stream>>arr[cnt]) cnt++;
    //然后两层for循环遍历取最大即可
    
<br><br>
### W - Prime Time  <br>
给定公式<br>
    
    n^2+n+41 produces a prime for 0 ≤ n < 40. For n = 40, the formula produces 1681, which is 41*41
    
    for n ≤ 10000000, there are 47,5% of primes produced by the formula
    
输入ab 求出在区间a<=n<=b的n算出的结果是素数的概率<br>
先素数打表(其实没有存进表 只是利用了vis数组)<br>
for循环从a到b直接枚举判断是不是素数(vis[i])<br>
然后 printf("%.2f\n",sum*1.0/(b-a+1)*100+1e-8); 即可<br>

<br><br>
### X - The equation SGU - 106  todo <br>
todo<br>

<br><br>
### Y - Farey Sequence  POJ - 2478 <br>
欧拉函数打表 <br>
给你一个数n 对于0 < a < b <= n 求真分数a/b的个数<br>
因为a/b为真分数 所以a和b互质 求真分数a/b的个数也即求<br>
0 < i <= n中 小于i的正整数中 有多少个与i互质的数<br>
累加起来就是真分数a/b的个数<br>
    
    ans=0;
    for(int i=2;i<=n;i++) ans+=phi[i];
    
<br><br>
### Z - The Super Powers UVA - 11752 again <br>
超级幂 求2^64-1范围内 可以是两个或两个以上的数的平方的数都有哪些输出<br>
数据范围1到 2^64 -1 可以看出需要用 unsigned long long <br>
其中1单独考虑 分析知满足条件的数必然是一个数的合数次方 最小是4 <br>
一个数的4次方在2^64 -1之内 那最大只能到65535 <br>
暴力枚举然后去除重复的就行了 可以用limit=ceil( 64/(log(i)/log(2)) )-1来判断一个数乘方数的上界<br>

去重此处用的是STL的set，用数组排序再用unique函数也可
<br><br>




