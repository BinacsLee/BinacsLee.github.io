## 题目链接 https://vjudge.net/contest/70325

### A - Number Sequence HDU - 1711 
基础KMP 返回第一次匹配的位置

### B - Oulipo HDU - 1686 
A串在B串中出现了几次 重复也算
      
      if(j==m){
            printf("%d\n",i-m+1);  //找到了 返回 可以改本函数返回类型
            j=f[j]; //若可重叠匹配
      }
      
### C - 剪花布条 HDU - 2087 
S串中有多少个T串 不可重叠
      
      if(j==m){
            printf("%d\n",i-m+1);  //找到了 返回 可以改本函数返回类型
            j=0; //  若不可重叠匹配
      }

### D - Cyclic Nacklace HDU - 3746 
给定一个字符串 所有字符全部循环最少两次 要加上多少个字符(即最重要形成一个有循环子串的串)<br>
next数组(普通未优化的next)求循环节 next[i]代表了前缀和后缀的最大匹配的值<br>
循环节长度 cirlen=len-next[len];<br>
(abcaabc 则循环节abca 诸如此)


### E - Period HDU - 1358 
题意： 一个字符串，从头到某个位置，字符串的前缀最多重复了多少次<br>
思路是先构造出 next[] 数组，下标为 i，定义一个变量 j = i - next[i] 就是next数组下标和下标对应值的差<br>
如果这个差能整除下标 i，即 i%j==0 ,则说明下标i之前的字符串（周期性字符串长度为 i）一定可以由一个前缀周期性的表示出来<br>
这个前缀的长度为刚才求得的那个差，即 j，则这个前缀出现的次数为 i/j 。所以最后输出i和i/j即可。

### F - The Minimum Length HUST - 1010 
求字符串的最短循环节 len-next[len]

### G - Power Strings POJ - 2406 
给定字符串 问最多由多少个相同子串组成(循环节)<br>
最小循环节cir=len-next[len] 如果len%cir==0 输出len/cir即可<br>
否则 若 cir不能整除len说明有剩余/循环节为整个长度 输出1(整串)

### H - Seek the Name, Seek the Fame POJ - 2752 
给定一个字符串s，从小到大输出s中既是前缀又是后缀的子串的长度。<br>
由next数组性质 倒推即可
      
      for(int i=len;i!=0;){
            ve[k++]=f[i];
            i=f[i];
      }
      for(int i=k-2;i>=0;i--) printf("%d ",ve[i]);
      printf("%d\n",len);
      
      
### I - Blue Jeans POJ - 3080 
找出n个串中最长的公共串 且要求字典序最大 答案是暴力 感觉无聊 没做//todo or not have to do
### J - Simpsons’ Hidden Talents HDU - 2594 
前后缀相同 给s1 s2求s1的最长前缀使其为s2的最长后缀 输出该串及长度<br>
想到next数组的含义 故把这两个串连接起来求next 另外注意所求串不能超过单个串的长度(跨越连接点)<br>
故使用<br>
    
    ans=next[len]
    while(ans>lenb||ans>lena) ans=next[ans];//直到长度小等于短串的长度 
    if(ans==0) printf("0\n");  
    else{  
        a[ans]=0;//去掉后面的就是前缀啦  
        printf("%s %d\n",a,ans);  
    } 
    
    //一说是while取next 一说是直接取最小 上下两种 都能过2333
    int len=strlen(P);
    int k=0;
    for(int i=len;i!=0;){
        ve[k++]=f[i];
        i=f[i];
    }
    for(int i=k-2;i>=0;i--) printf("%d ",ve[i]);
    printf("%d\n",len);
    

### K - Count the string HDU - 3336 
kmp+dp<br>
题意：给一串字符串 问这串字符串所有的前缀总共在这个字符串中出现了几次//again<br> 
        
        memset(a,0,sizeof(a));
        for(int i=1;i<=m;i++){
            a[i]=(a[f[i]]+1)%10007;
            sum=(sum+a[i])%10007;
        }
        printf("%d\n",sum);
        
        
        
### L - Clairewd’s message HDU - 4300 
拓展kmp 
        
        /*扩展kmp算法可以用o(n+m)的复杂度求出字符串s1的任意后缀与字符串s2的最长公共前缀*/  
        /*扩展kmp算法的next[i]==j表示s2的以s2[i]为起始的后缀与串本身的最长公共前缀长度*/  
        /*ex[i]为s1[i..]与s2的最长公共前缀，next[i]为s2[i..]与s2的最长公共前缀*/ 
        
将字符串解密然后模版即可
        
      
