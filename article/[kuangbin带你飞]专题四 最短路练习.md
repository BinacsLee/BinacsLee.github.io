## 2017-3-11～2017-3-14
## 题目链接 https://vjudge.net/contest/66569
### A POJ - 2387
寒假做过 简单最短路 有重边WA了一发
### B POJ - 2253
‘dijkstra变形 d[i]表示从源点到i的最短路径的最大边的值 ‘
    
    int v=-1;
    for(int i=0;i<n;i++){
        if(!vis[i]&&(v==-1||d[i]<d[v])) v=i;
        if(v==-1) break;
        vis[v]=true;
        for(int i=0;i<n;i++){
            if(!vis[i]&&d[i]>max(d[v],maps[v][i])) d[i]=max(d[v],maps[v][i]);
        }
    }
    
### C POJ - 1797
‘dijkstra变形 d[i]表示源点到i的最长路径的最短边的值 ’
    
    
    int v=-1;
    for(int i=1;i<=n;i++){
        if(!vis[i]&&(v==-1||d[i]>d[v])) v=i;
        if(v==-1) break;
        vis[v]=true;
        for(int i=1;i<=n;i++)
            if(!vis[i]&&cost[v][i]!=INF&&d[i]<min(cost[v][i],d[v])){ 
                //因为并不是都可达 没有写cost[v][i]!=INF(不可达 WA
                d[i]=min(cost[v][i],d[v]);
            }
     }


### D POJ - 3268
寒假做过矩阵转置前后两次最短路 求和即可
### E POJ - 1860 
bellman判‘正’环 写法可以是
    
    for(int j=1;j<=n-1;j++) //执行n-1次 然后
    
    for(int i=1;i<=tot;i++)
        if(d[e[i].b]<(d[e[i].a]-e[i].c)*e[i].r) return false;
        
        
        
     
### F POJ - 3259 
寒假做过 wormhole 判负环 
### G POJ - 1502
最短路dijkstra
     
    if(c[0]!='x')
        cost[i][j]=cost[j][i]=atoi(c); //atoi字符型转化int
    
### H POJ - 3660 
floyd变形 或运算 确定某个奶牛的名次即该奶牛胜负(0/1 个数之和为n-1
    
    for(int i=1;i<=n;i++)
        if(i!=s&&(able[s][i]||able[i][s])) cnt++;
    if(cnt==n-1) return true;
    return false;
    
### I POJ - 2240 
floyd变形 cost初始化0 判定从某个点开始能否回到该点时增加了
     
    if(cost[i][j]<cost[i][k]*cost[k][j]) cost[i][j]=cost[i][k]*cost[k][j];
    //松弛条件
    
    for(int i=1;i<=n;i++)
        if(cost[i][i]>1) return true;
    return false;
     
    
### K POJ - 1511
2次spfa //see again
### L POJ - 2502 
dijkstra 输入处理有点麻烦 闲着有空可以考虑再看看
### M POJ - 1062 
昂贵的聘礼典型最短路 </br>
处理注意 因为要求所有参与兑换的人的等级差值不能超过m 故枚举所有最高等级数进行dijkstra 最后得到最小值
       
    for(int i=1;i<=n;i++){
        if(levv<lev[i]||levv-lev[i]>m) vis[i]=true;
        else vis[i]=false;
    }
    //不能在循环内修改cost值 一开始这样WA 注意这里初始化vis的巧妙作用
    
### N POJ - 1847
简单dijkstra 
### O LightOJ - 1074
bellman_ford+简单dfs //主要是bellman邻接表没弄熟= = 闲着无聊可以再看看
### P HDU - 4725 
spfa 建图 
 1. 两层都出现过点相邻层才建边
 2. 层到点建边  点到相邻层建边
 3. 点到点建边
 
### QRS以及J 
差分约束 暂时没做
    
    
    
