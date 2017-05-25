###2017-02-18 
###题目链接 https://vjudge.net/contest/149933

// (H) I 待解决


## A CodeForces - 377A
要往可行的方格中填充X 同时保持剩下的方格的连通性</br>
dfs 回溯的时候填充X</br>
WA 1 智障应该 if(u<=0||u>n) break;   ..  写成 if(u<0||u>=n) break;  </br>

## B CodeForces - 445A
可行空格填充W/B 可能有多解 任意输出一解</br>
Solution 1 dfs 这是正常思维</br>
Solution 2 i行j列 只要斜着填就行 即</br>

    if((i+j)%2) map[i][j]='B';
    else map[i][j]='W';
    
    
WA 1 内层循环条件写错...m写成了n...</br>

## C POJ - 3278
计步数从n到k 每次x+1/x-1／x*2 </br>
bfs </br>
WA 1 判断出界(>100005) 即
    
    if(nexttem<0||nexttem>100005)写成了if(nexttem<0||nexttem>k) WA了无数发....醉....
    
    
    
## D CodeForces - 598B
操作右移字符串的一部分(shift </br>
暴力操作即可 </br>

## E CodeForces - 412C
暴力处理串即可</br>
WA 1 :
    
    for(int i=1;i<n;i++)写成了for(int i=1;i<s[0].length();i++) WA了一发...
    
    
## F CodeForces - 598D
dfs </br>
注意的是 test10 TLE </br>
EXP 1 vis由bool数组改为int数组(初始化0 每次计算连通量时给vis赋值为id 减少重复dfs计算次数 </br>
一开始思路错了 抽象想的时候误以为某个’*‘可以被多次访问了= =
    
## G - Rivals SPOJ - RIVALS
快速幂 另外有点数学结论的感觉？？
    
        for(int i=1;i<=2*1e6;i++)
        fact[i]=(fact[i-1]*i)%mod;
        int t;
        cin>>t;
        while(t--){
            int n,m;
            scanf("%d%d",&n,&m);
            ll s=(fact[n+m]*mod_pow(fact[n],mod-2))%mod;
            s=s*mod_pow(fact[m],mod-2);
            printf("%lld\n",s%mod);
        }
    
    
    
## H - String Problem CodeForces - 33B 

不知道为啥老RE啊。。。崩溃
<br><br>
I没写

